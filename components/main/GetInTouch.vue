<template lang="pug">
   section.get-in-touch
    h2.get-in-touch__title GET IN TOUCH
    h3.get-in-touch__subtitle For clients
    a(href="mailto:support@cheese-software.com").get-in-touch__email support@cheese-software.com

    ul.get-in-touch__policy-list
        li(v-for="(item, index) in items" :key="index").get-in-touch__policy-item
            p.get-in-touch__policy-item-text {{item.text}}
    
</template>

<script>
export default {
  data() {
    return {
      items: [
        {
          id: 0,
          text: "Terms of use",
        },
        {
          id: 1,
          text: "Privacy Policy",
        },
        {
          id: 2,
          text: "Contacts",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.get-in-touch {
  padding: 0 4.267vw 8.533vw;
  &__title {
    width: 53.333vw;
    text-transform: uppercase;
    font-weight: 700;
    font-size: 11.733vw;
    line-height: 1;
    letter-spacing: 0.01em;
    color: #ffa600;
  }

  &__subtitle {
    margin: 8.533vw 0 0 0;
    color: #ffa600;
    font-weight: 500;
    font-size: 3.733vw;
    line-height: 1.4;
  }

  &__email {
    margin: 2.133vw 0 0 0;
    font-weight: 500;
    font-size: 5.6vw;
    line-height: 1.3;
    letter-spacing: -0.03em;

    color: #ffffff;
  }

  &__policy-list {
    margin: 12.8vw 0 0 0;
  }
  &__policy-item {
    font-style: normal;
    font-weight: 600;
    font-size: 4.8vw;
    line-height: 1.2;

    letter-spacing: 0.01em;
    text-decoration-line: underline;

    color: #ffffff;

    &:not(:first-child) {
      margin: 4.267vw 0 0 0;
    }
  }
}
</style>
