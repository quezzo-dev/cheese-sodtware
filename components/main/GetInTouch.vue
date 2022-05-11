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

  @media screen and (min-width: 768px) {
    padding: 0 4.167vw 5.469vw;
  }

  @media screen and (min-width: 1440px) {
    padding: 0 9.028vw 5vw;
  }

  &__title {
    width: 53.333vw;
    text-transform: uppercase;
    font-weight: 700;
    font-size: 11.733vw;
    line-height: 1;
    letter-spacing: 0.01em;
    color: #ffa600;

    @media screen and (min-width: 768px) {
      font-size: 5.729vw;
      width: auto;
    }

    @media screen and (min-width: 1440px) {
      font-size: 5vw;
    }
  }

  &__subtitle {
    margin: 8.533vw 0 0 0;
    color: #ffa600;
    font-weight: 500;
    font-size: 3.733vw;
    line-height: 1.4;

    @media screen and (min-width: 768px) {
      margin: 5.208vw 0 0 0;
      font-size: 1.823vw;
    }

    @media screen and (min-width: 1440px) {
      margin: 3.889vw 0 0 0;
      font-size: 1.528vw;
    }
  }

  &__email {
    margin: 2.133vw 0 0 0;
    font-weight: 500;
    font-size: 5.6vw;
    line-height: 1.3;
    letter-spacing: -0.03em;

    color: #ffffff;

    @media screen and (min-width: 768px) {
      font-size: 2.734vw;
    }

    @media screen and (min-width: 1440px) {
      font-size: 2.778vw;
    }
  }

  &__policy-list {
    margin: 12.8vw 0 0 0;

    @media screen and (min-width: 768px) {
      margin: 7.813vw 0 0 0;
    }

    @media screen and (min-width: 1440px) {
      margin: 5.556vw 0 0 0;
    }
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

    @media screen and (min-width: 768px) {
      font-size: 2.344vw;

      &:not(:first-child) {
        margin: 2.083vw 0 0 0;
      }
    }

    @media screen and (min-width: 1440px) {
      font-size: 2.5vw;

      &:not(:first-child) {
        margin: 1.111vw 0 0 0;
      }
    }
  }
}
</style>
