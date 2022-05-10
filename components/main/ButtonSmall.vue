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
  width: 26.667vw;
  background: #fff;
  color: #ffa600;
  border-radius: 4.267vw;
  height: 10.4vw;
  font-size: 3.733vw;
  text-transform: uppercase;
  //   letter-spacing: 0.1em;
  font-weight: 700;
}
</style>
