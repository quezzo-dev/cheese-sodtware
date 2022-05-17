<template lang="pug">
    section.hero
      client-only
        .hero__section-wrapper
          .mySwiper(v-swiper:mySwiper="swiperOption" ref="mySwiperRef" )
              .swiper-wrapper
                  li(v-for="(item, index) in items" :key="index").hero__slide.swiper-slide
                          .hero__bg-wrapper
                              img(:src="item.bgImage").hero__slide-img
                              .hero__bg
                          .hero__slide-content
                              h2.hero__slide-title {{item.title}}
                              p.hero__slide-text {{item.text}}
                              Button.hero__button
          .hero__desk-wrapper
            .hero__desk-bg-wrapper
              img(src="@/assets/images/hero/rustHeroDesk.jpg").hero__desk-bg
              .hero__bg
            .hero__slide-content
              h2.hero__slide-title Rust
              p.hero__slide-text Experimental Hack v1.2
              Button.hero__button
              script(
      src="https://telegram.org/js/telegram-widget.js?19"
      :data-telegram-login="BOT_USERNAME"
      data-size="medium"
      :data-onauth="onTelegramAuth(user)"
      data-request-access="write")
  
            .hero__desk-card-wrapper
              ul.hero__desk-list
                  li.hero__desk-card(v-for="(card, index) in cards" :key="index")
                    img(:src="card.img").hero__desk-card-img
                    .hero__desk-card-content
                      h2.hero__desk-card-title {{card.title}}
                      ButtonSmall(:btnText="card.btnText")

                            

        

</template>
<script
  async
  src="https://telegram.org/js/telegram-widget.js?19"
  data-telegram-login="samplebot"
  data-size="large"
  :data-onauth="onTelegramAuth(user)"
  data-request-access="write"
></script>

<script>
import Button from "@/components/main/ButtonBig.vue";
import ButtonSmall from "@/components/main/ButtonSmall.vue";

export default {
  components: {
    Button,
    ButtonSmall,
  },

  mounted() {
    alert("New2");

    // this.onTelegramAuth();
  },

  methods: {
    onTelegramAuth(user) {
      console.log(
        "Logged in as " +
          user.first_name +
          " " +
          user.last_name +
          " (" +
          user.id +
          (user.username ? ", @" + user.username : "") +
          ")"
      );
    },
  },

  data() {
    return {
      BOT_USERNAME: "gerchik_login_bot",
      BOT_TOKEN: "5295915260:AAEnm4WCPpYdK7T6pIA8uaGfdhTrh7sogFY",
      REDIRECT_URI: "https://cheese-software.netlify.app/",
      items: [
        {
          id: 0,
          title: "Rust",
          text: "Experimental Hack v1.2",
          btnLink: "",
          bgImage: require("@/assets/images/hero/image1.jpg"),
        },
        {
          id: 1,
          title: "Rust",
          text: "Hack",
          btnLink: "",
          bgImage: require("@/assets/images/hero/image1.jpg"),
        },
      ],

      cards: [
        {
          id: 0,
          title: "Rust",
          btnLink: "",
          img: require("@/assets/images/catalog/rust.jpg"),
          btnText: "open",
        },
        {
          id: 1,
          title: "Rust",
          btnLink: "",
          img: require("@/assets/images/catalog/rust.jpg"),
          btnText: "open",
        },
        // {
        //   id: 2,
        //   title: "Rust",
        //   btnLink: "",
        //   img: require("@/assets/images/catalog/rust.jpg"),
        //   btnText: "open",
        // },
      ],
      swiperOption: {
        slidesPerView: 1,
        spaceBetween: 0,
        loop: true,
        // pagination: {
        //   el: ".swiper-pagination",
        // },
        // slideToClickedSlide: true,
        navigation: {
          nextEl: ".swiper-button-prev",
          prevEl: ".swiper-button-next",
        },
      },
    };
  },
};
</script>

<style lang="scss" scoped>
.hero {
  padding: 16vw 0 0 0;
  @media screen and (min-width: 768px) {
    padding: 7.813vw 0 0 0;
  }

  @media screen and (min-width: 1440px) {
    padding: 5.556vw 0 0 0;
  }
  overflow-x: hidden;
  &__section-wrapper {
    width: 100%;
  }

  &__slide {
    position: relative;
  }

  &__slide-content {
    position: absolute;
    top: 18.667vw;
    left: 4.267vw;

    @media screen and (min-width: 768px) {
      top: 16.927vw;
      left: 4.167vw;
    }
    @media screen and (min-width: 1440px) {
      top: 13.889vw;
      left: 9.028vw;
    }
  }

  &__slide-img {
    width: 100%;
    height: auto;
    filter: blur(2px);
  }

  &__slide-title {
    font-size: 16vw;
    font-weight: 700;
    color: #ffa600;
    line-height: 1;

    @media screen and (min-width: 768px) {
      font-size: 9.896vw;
    }

    @media screen and (min-width: 1440px) {
      font-size: 6.667vw;
    }
  }

  &__slide-text {
    margin: 4.267vw 0 0 0;
    font-weight: 500;
    line-height: 1;
    font-size: 8.533vw;
    color: #fff;

    @media screen and (min-width: 768px) {
      margin: 2.083vw 0 0 0;
      font-size: 5.208vw;
      width: 37.109vw;
    }

    @media screen and (min-width: 768px) {
      margin: 2.222vw 0 0 0;
      font-size: 4.167vw;
      width: 30.139vw;
    }
  }

  &__bg {
    background-color: rgba(0, 0, 0, 0.3);
    height: 100%;
    position: absolute;
    width: 100%;
    top: 0;
    left: 0;
  }

  &__button {
    margin: 69.867vw 0 0 0;

    @media screen and (min-width: 768px) {
      margin: 4.167vw 0 0 0;
    }

    @media screen and (min-width: 1440px) {
      margin: 2.222vw 0 0 0;
    }
  }

  &__desk-wrapper {
    display: none;
    @media screen and (min-width: 768px) {
      position: relative;

      display: block;
    }
  }

  &__desk-bg {
    width: 100%;
    filter: blur(2px);
  }

  &__desk-bg-wrapper {
    position: relative;
    @media screen and (min-width: 1440px) {
      overflow: hidden;
      height: 100vh;
    }
  }

  &__desk-card-wrapper {
    // overflow-x: auto;
    // width: 100%;

    position: absolute;
    top: 13.021vw;
    right: 4.167vw;

    @media screen and (min-width: 1440px) {
      top: 13.889vw;
      right: 9.028vw;
    }
  }

  &__desk-list {
    display: flex;
  }

  &__desk-card {
    background: rgba(22, 22, 22, 0.7);

    border: 0.267vw solid #ffa600;
    border-radius: 4.267vw;

    &:not(:first-child) {
      margin: 6.4vw 0 0 0;
    }

    @media screen and (max-width: 1439px) {
      &:last-child {
        display: none;
      }
    }

    @media screen and (min-width: 768px) {
      border-radius: 2.083vw;
      width: 32.552vw;
      margin: 0;
      // &:not(:last-child) {
      //   margin: 0 3.125vw 0 0;
      // }
      &:not(:first-child) {
        margin: 0 0 0 0;
      }
    }

    @media screen and (min-width: 1440px) {
      width: 20.833vw;
      border-radius: 1.111vw;

      &:not(:last-child) {
        margin: 0 2.778vw 0 0;
      }
    }
  }

  &__desk-card-img {
    border-radius: 4.267vw 4.267vw 0 0;
    width: 100%;

    @media screen and (min-width: 768px) {
      border-radius: 2.083vw 2.083vw 0 0;
    }
  }

  &__desk-card-title {
    color: #fff;
    font-weight: 700;
    font-size: 8.8vw;
    line-height: 1;
    letter-spacing: 0.01em;

    @media screen and (min-width: 768px) {
      font-size: 4.688vw;
    }

    @media screen and (min-width: 1440px) {
      font-size: 2.292vw;
    }
  }

  &__desk-card-content {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 4.267vw;

    @media screen and (min-width: 768px) {
      padding: 2.083vw;
    }
    @media screen and (min-width: 1440px) {
      padding: 1.111vw;
    }
  }
}

.mySwiper {
  @media screen and (min-width: 768px) {
    display: none;
  }
}
</style>
