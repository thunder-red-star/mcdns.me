<template>
  <!-- Title Element -->
  <!-- Contains a brand name, title, subtitle, and optional buttons -->
  <div class="title-content">
    <h1 class="title">{{ title }}</h1>
    <p class="subtitle">{{ subtitle }}</p>
    <LinkButton
      v-if="buttonText"
      :text="buttonText"
      :link="buttonLink"
    />
  </div>
</template>

<script>
import LinkButton from "../elements/LinkButton";
import Typography from "../elements/Typography";

export default {
  name: 'TitleElement',
  components: {LinkButton},
  props: {
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
  .title-content {
    text-align: center;
    padding: 0 40px;
  }
</style>