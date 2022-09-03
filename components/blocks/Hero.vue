<template>
  <!-- Hero Template -->
  <!-- A hero block is an image background with a text overlay, and optionally a button. -->
  <!-- The text overlay is centered and vertically aligned. -->
  <!-- The button is under the text overlay. -->
  <div class="hero">
    <div class="hero-body">
      <div class="container">
        <h1 class="title">
          {{ title }}
        </h1>
        <p class="subtitle">
          {{ subtitle }}
        </p>
        <a class="button is-primary is-large" href="{{ buttonLink }}">
          {{ buttonText }}
        </a>
      </div>
    </div>
  </div>
</template>

<script>
</script>

<style scoped lang="scss">
  .hero {
    background-image: url({{ backgroundImage }});
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
  }
</style>