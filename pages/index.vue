<template lang="pug">
  .page
    Header
    Hero
    Catalog
    GetInTouch
    Footer

</template>

<script>
import Header from "@/components/main/Header.vue";
import Hero from "@/components/main/Hero.vue";
import Catalog from "@/components/main/Catalog.vue";
import GetInTouch from "@/components/main/GetInTouch.vue";
import Footer from "@/components/main/Footer.vue";

export default {
  mounted() {},

  methods: {},

  data() {
    return {
      title: "Zagolovok",
    };
  },

  components: {
    Header,
    Hero,
    Catalog,
    GetInTouch,
    Footer,
  },
};
</script>

<style lang="scss" scoped></style>
