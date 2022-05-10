<template lang="pug">
    section.hero
        .hero__section-wrapper
                            .mySwiper(v-swiper:mySwiper="swiperOption")
                                .swiper-wrapper
                                    li(v-for="(item, index) in items" :key="index").hero__slide.swiper-slide
                                            .hero__bg-wrapper
                                                img(:src="item.bgImage").hero__slide-img
                                                .hero__bg
                                            .hero__slide-content
                                                h2.hero__slide-title {{item.title}}
                                                p.hero__slide-text {{item.text}}
                                                Button.hero__button
                                    .swiper-pagination.swiper-pagination-bullets
        

</template>

<script>
import Button from "@/components/main/ButtonBig.vue";
export default {
  components: {
    Button,
  },
  data() {
    return {
      items: [
        {
          id: 0,
          title: "Rust",
          text: "Experemental Hack v1.2",
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
      swiperOption: {
        slidesPerView: 1,
        spaceBetween: 0,
        loop: true,
        pagination: {
          el: ".swiper-pagination",
        },
      },
    };
  },
};
</script>

<style lang="scss" scoped>
.hero {
  padding: 16vw 0 0 0;
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
  }

  &__slide-text {
    margin: 4.267vw 0 0 0;
    font-weight: 500;
    line-height: 1;
    font-size: 8.533vw;
    color: #fff;
  }

  &__bg {
    background-color: rgba(0, 0, 0, 0.3);
    height: 100%;
    position: fixed;
    width: 100%;
    top: 0;
    left: 0;
  }

  &__button {
    margin: 69.867vw 0 0 0;
  }
}
</style>
