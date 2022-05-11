<template lang="pug">
    footer.footer
        template(v-if="width < 768")
            nuxt-link(to="/")
                img(src="@/assets/images/header/logo-small.svg")
        template(v-else)
            nuxt-link(to="/")
                img(src="@/assets/images/header/logo.svg").footer__logo
        p.footer__text Designed by SAUREN & Developed by VARTO GROUP
        p.footer__copy © 2022
</template>

<script>
export default {
  data() {
    return {
      width: 0,
    };
  },

  mounted() {
    this.width = window.innerWidth;
    console.log(this.width);
  },
};
</script>

<style lang="scss" scoped>
.footer {
  padding: 0 4.267vw 8.533vw;

  @media screen and (min-width: 768px) {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  @media screen and (min-width: 768px) {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 0 9.028vw 3.889vw;
  }

  &__text {
    margin: 4.267vw 0 0 0;
    width: 54.2vw;
    font-style: normal;
    font-weight: 400;
    font-size: 3.733vw;
    line-height: 140%;
    /* or 20px */

    color: #ffffff;

    @media screen and (min-width: 768px) {
      font-size: 1.693vw;
      margin: 0;
      width: auto;
    }

    @media screen and (min-width: 1440px) {
      font-size: 1.528vw;
    }
  }

  &__copy {
    margin: 6.4vw 0 0 0;
    font-style: normal;
    font-weight: 400;
    font-size: 6.4vw;
    line-height: 131%;
    /* or 31px */
    color: #ffffff;

    @media screen and (min-width: 768px) {
      margin: 0;
      font-size: 3.125vw;
    }

    @media screen and (min-width: 1440px) {
      font-size: 3.056vw;
    }
  }

  &__logo {
    @media screen and (min-width: 1440px) {
      width: 12.5vw;
    }
  }
}
</style>
