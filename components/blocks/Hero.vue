<template>
  <!-- Hero Template -->
  <!-- A hero block is an image background with a text overlay, and optionally a button. -->
  <!-- The text overlay is centered and vertically aligned. -->
  <!-- The button is under the text overlay. -->
  <div class="hero" v-bind:style="'background-image: url(' + backgroundImage + ')'">
    <div class="hero-body">
      <div class="container">
        <h1 class="title">
          {{ title }}
        </h1>
        <p class="subtitle">
          {{ subtitle }}
        </p>
        <LinkButton
          v-if="buttonText"
          :text="buttonText"
          :link="buttonLink"
        />
      </div>
    </div>
  </div>
</template>

<script>
import LinkButton from "../elements/LinkButton";
export default {
  name: 'Hero',
  components: {LinkButton},
  props: {
    backgroundImage: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    subtitle: {
      type: String,
      required: true,
    },
    buttonText: {
      type: String,
      required: true,
    },
    buttonLink: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped lang="scss">
  .hero {
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    width: 100%;
    height: 100vh;
  }

  .hero-body {
    background-color: rgba(255, 255, 255, 0.7);
    width: 100%;
    height: 100%;
    position: relative;
    display: flex;
    text-align: center;
    align-items: center;
    justify-content: center;
    vertical-align: middle;
  }

  .container {
    /* hack™️ */
    max-width: 960px;
    margin: 0 auto;
  }

  .title {
    font-size: min(10vw, 4rem);
  }

  .subtitle {
    font-size: min(5vw, 1.3rem);
  }

  .button {
    margin-top: 3rem;
  }
</style>