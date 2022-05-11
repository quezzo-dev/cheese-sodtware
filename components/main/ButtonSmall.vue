<template lang="pug">
    button.button {{btnText}}

</template>

<script>
export default {
  props: ["btnText"],
};
</script>

<style lang="scss" scoped>
.button {
  cursor: pointer;
  width: 26.667vw;
  background: #fff;
  color: #ffa600;
  border-radius: 4.267vw;
  height: 10.4vw;
  font-size: 3.733vw;
  text-transform: uppercase;
  //   letter-spacing: 0.1em;
  font-weight: 700;

  @media screen and (min-width: 768px) {
    width: 13.021vw;
    font-size: 1.823vw;
    height: 5.078vw;
  }

  @media screen and (min-width: 1440px) {
    width: 6.944vw;
    height: 2.639vw;
    font-size: 0.972vw;
  }
}
</style>
