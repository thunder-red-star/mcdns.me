<template>
  <!-- Typography Element -->
  <!-- Displays text in a variety of styles, so we can keep formatting in one place -->
  <p v-bind:class="variant">
    <slot />
  </p>
</template>

<script>
export default {
  name: 'Typography',
  props: {
    variant: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped lang="scss">
  .title {
    font-size: max(min(4rem, 8vw), 2rem);
    font-weight: 700;
    line-height: 1.2;
  }

  .subtitle {
    font-size: max(min(1.5rem, 3vw), 1.2rem);
    font-weight: 400;
    line-height: 1.2;
  }

  .body {
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.5;
  }

  .caption {
    font-size: min(max(1rem, 2vw), 0.8rem);
    font-weight: 400;
    line-height: 1.5;
  }

  .h1 {
    font-size: min(max(5rem, 10vw), 2rem);
    font-weight: 700;
    line-height: 1.2;
  }

  .h2 {
    font-size: min(max(4rem, 8vw), 1.8rem);
    font-weight: 700;
    line-height: 1.2;
  }

  .h3 {
    font-size: min(max(3rem, 6vw), 1.6rem);
    font-weight: 700;
    line-height: 1.2;
  }

  .h4 {
    font-size: min(max(2rem, 4vw), 1.4rem);
    font-weight: 700;
    line-height: 1.2;
  }

  .h5 {
    font-size: min(max(1.5rem, 3vw), 1.2rem);
    font-weight: 700;
    line-height: 1.2;
  }

  .h6 {
    font-size: min(max(1.2rem, 2vw), 1rem);
    font-weight: 700;
    line-height: 1.2;
  }

  .p {
    font-size: 1rem;
    font-weight: 400;
    line-height: 1.5;
  }

  .small {
    font-size: 0.875rem;
    font-weight: 400;
    line-height: 1.5;
  }

  .span {
    font-size: 0.875rem;
    font-weight: 400;
    line-height: 1.5;
  }

  * {
    font-family: 'Inter', Segoe UI, Roboto, Helvetica, Arial, sans-serif;
  }
</style>