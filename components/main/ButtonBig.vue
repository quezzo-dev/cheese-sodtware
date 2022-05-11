<template lang="pug">
    button.button Download Now
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
.button {
  cursor: pointer;

  width: 55.267vw;
  background: #ffa600;
  color: #fff;
  border-radius: 4.267vw;
  height: 16vw;
  font-size: 4.8vw;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  font-weight: 700;

  @media screen and (min-width: 768px) {
    width: 27.615vw;
    height: 7.813vw;
    font-size: 2.344vw;
    border-radius: 2.083vw;
  }

  @media screen and (min-width: 1440px) {
    width: 20.833vw;
    border-radius: 1.111vw;
    height: 5.556vw;
    font-size: 1.667vw;
  }
}
</style>
