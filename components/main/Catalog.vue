<template lang="pug">
    section.catalog
        h2.catalog__title Game catalog
        ul.catalog__list
          li.catalog__item(v-for="(item, index) in items" :key="index")
            img(:src="item.img").catalog__img
            .catalog__item-content
              h2.catalog__item-title {{item.title}}
              Button(:btnText="item.btnText")

</template>

<script>
import Button from "@/components/main/ButtonSmall.vue";
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
        {
          id: 2,
          title: "Rust",
          btnLink: "",
          img: require("@/assets/images/catalog/rust.jpg"),
          btnText: "open",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.catalog {
  padding: 8.533vw 4.267vw;

  @media screen and (min-width: 768px) {
    padding: 5.469vw 4.167vw;
  }

  @media screen and (min-width: 1440px) {
    padding: 5vw 9.028vw;
  }
  &__title {
    width: 53.333vw;
    text-transform: uppercase;
    font-weight: 700;
    font-size: 11.733vw;
    line-height: 1;
    letter-spacing: 0.01em;
    color: #ffa600;

    @media screen and (min-width: 768px) {
      font-size: 5.729vw;
      width: auto;
    }

    @media screen and (min-width: 1440px) {
      font-size: 5vw;
    }
  }

  &__list {
    margin: 4.267vw 0 0 0;

    @media screen and (min-width: 768px) {
      margin: 4.167vw 0 0 0;
      display: grid;
      grid-template-columns: 1fr 1fr;
      grid-gap: 2.604vw;
    }

    @media screen and (min-width: 1440px) {
      margin: 5.556vw 0 0 0;
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      grid-gap: 4.861vw;
    }
  }

  &__item {
    border: 0.267vw solid #ffa600;
    border-radius: 4.267vw;

    &:not(:first-child) {
      margin: 6.4vw 0 0 0;
    }

    @media screen and (min-width: 768px) {
      border-radius: 2.083vw;
      width: 44.271vw;
      &:not(:first-child) {
        margin: 0;
      }
    }

    @media screen and (min-width: 1440px) {
      width: 23.75vw;
      border-radius: 1.111vw;
    }
  }

  &__img {
    border-radius: 4.267vw 4.267vw 0 0;
    width: 100%;

    @media screen and (min-width: 768px) {
      border-radius: 2.083vw 2.083vw 0 0;
    }

    @media screen and (min-width: 1440px) {
      border-radius: 1.111vw 1.111vw 0 0;
    }
  }

  &__item-title {
    color: #fff;
    font-weight: 700;
    font-size: 8.8vw;
    line-height: 1;
    letter-spacing: 0.01em;

    @media screen and (min-width: 768px) {
      font-size: 4.688vw;
    }

    @media screen and (min-width: 1440px) {
      font-size: 3.056vw;
    }
  }

  &__item-content {
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
</style>
