<template lang="pug">
  .page
    Header
    Hero
    Catalog

</template>

<script>
import Header from "@/components/main/Header.vue";
import Hero from "@/components/main/Hero.vue";
import Catalog from "@/components/main/Catalog.vue";

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
  },
};
</script>

<style lang="scss" scoped></style>
