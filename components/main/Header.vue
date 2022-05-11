<template lang="pug">
    header.header
        nuxt-link(to="/")
            img(src="@/assets/images/header/logo.svg").header__logo-img
        button(@click="hidden = !hidden").header__burger-menu
            template(v-if="hidden")
                img(src="@/assets/images/header/burger-menu.svg").header__burger-menu-svg
            template(v-else)
                img(src="@/assets/images/header/burger-cross.svg").header__burger-menu-svg            
        div(:class="{'hide' : hidden} ").header__mobile-nav
            ul.header__mobile-nav-list
                li(v-for="item in items").header__mobile-nav-item {{item.text}}
        ul.header__nav-list
          li(v-for="item in items").header__nav-item {{item.text}}
            



</template>

<script>
export default {
  data() {
    return {
      hidden: true,
      items: [
        { id: 0, text: "status" },
        { id: 1, text: "about us" },
        { id: 2, text: "faq" },
        { id: 3, text: "catalog" },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.header {
  padding: 0 4.267vw;
  z-index: 2;

  position: fixed;
  width: 100%;
  top: 0;
  left: 0;
  height: 16vw;
  background: #161616;

  display: flex;
  justify-content: space-between;
  align-items: center;

  @media screen and (min-width: 768px) {
    height: 7.813vw;
    padding: 0 4.167vw;
  }

  @media screen and (min-width: 1440px) {
    height: 5.556vw;
    padding: 0 9.028vw;
  }

  &__mobile-nav {
    position: absolute;
    z-index: -1;
    top: 0;
    left: 0;
    width: 100%;
    height: 100vh;
    background: #161616;
  }

  &__logo-img {
    @media screen and (min-width: 1440px) {
      width: 12.5vw;
    }
  }

  &__mobile-nav-list {
    color: #ffa600;
    padding: 16vw 4.267vw;
  }

  &__mobile-nav-item {
    text-transform: uppercase;
    font-size: 9.6vw;
    font-weight: 700;
    letter-spacing: 0.06em;

    &:not(:first-child) {
      margin: 4.267vw 0 0 0;
    }
  }

  &__burger-menu {
    @media screen and (min-width: 768px) {
      display: none;
    }
  }

  &__nav-list {
    color: #ffa600;
    display: none;
    @media screen and (min-width: 768px) {
      display: flex;
      align-items: center;
    }

    // @media screen and () {
    // }
  }

  &__nav-item {
    text-transform: uppercase;
    font-weight: 700;
    font-size: 2.083vw;
    line-height: 160%;

    letter-spacing: 0.01em;

    &:not(:last-child) {
      margin: 0 3.125vw 0 0;
    }

    @media screen and (min-width: 1440px) {
      font-size: 1.25vw;
    }
  }

  &__burger-menu-svg {
    width: 25px;
  }
}

.hide {
  display: none;
}
</style>
