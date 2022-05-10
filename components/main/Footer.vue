<template lang="pug">
    footer.footer
        nuxt-link(to="/")
            img(src="@/assets/images/header/logo-small.svg")
        p.footer__text Designed by SAUREN & Developed by VARTO GROUP
        p.footer__copy © 2022
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.footer {
  padding: 0 4.267vw 8.533vw;

  &__text {
    margin: 4.267vw 0 0 0;
    width: 54.2vw;
    font-style: normal;
    font-weight: 400;
    font-size: 3.733vw;
    line-height: 140%;
    /* or 20px */

    color: #ffffff;
  }

  &__copy {
    margin: 6.4vw 0 0 0;
    font-style: normal;
    font-weight: 400;
    font-size: 6.4vw;
    line-height: 131%;
    /* or 31px */

    color: #ffffff;
  }
}
</style>
