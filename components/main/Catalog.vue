<template lang="pug">
    .catalog
        .catalog__title Game catalog
        ul.catalog__list
          li.catalog__item(v-for="(item, index) in items" :key="index")
            img(:src="item.img").catalog__img
            .catalog__item-content
              h2.catalog__item-title {{item.title}}

</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          id: 0,
          title: "Rust",
          btnLink: "",
          img: require("@/assets/images/catalog/rust.jpg"),
        },
        {
          id: 1,
          title: "Rust",
          btnLink: "",
          img: require("@/assets/images/catalog/rust.jpg"),
        },
        {
          id: 2,
          title: "Rust",
          btnLink: "",
          img: require("@/assets/images/catalog/rust.jpg"),
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.catalog {
  padding: 8.533vw 4.267vw;
  &__title {
    width: 53.333vw;
    text-transform: uppercase;
    font-weight: 700;
    font-size: 11.733vw;
    line-height: 1;
    letter-spacing: 0.01em;
    color: #ffa600;
  }

  &__list {
    margin: 4.267vw 0 0 0;
  }

  &__item {
    border: 0.267vw solid #ffa600;
    border-radius: 4.267vw;

    &:not(:first-child) {
      margin: 6.4vw 0 0 0;
    }
  }

  &__img {
    border-radius: 4.267vw 4.267vw 0 0;
    width: 100%;
  }

  &__item-title {
    color: #fff;
    font-weight: 700;
    font-size: 11.733vw;
    line-height: 1;
    letter-spacing: 0.01em;
  }

  &__item-content {
    padding: 4.267vw;
  }
}
</style>
