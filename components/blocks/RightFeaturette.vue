<template>
  <!-- Featurette Template -->
  <!-- A featurette is a block of content with text on either the left or right side, and an image on the opposite side. -->
  <!-- The text is aligned to the left or right side, and the image is aligned to the opposite side. -->
  <!-- If the viewport is too small, the image will be above the text in a single column. -->
  <!-- You can use Tailwind's flexbox utilities to change the order of the image and text. -->
  <div class="featurette flex flex-wrap place-items-center">
    <div class="featurette-image w-full md:w-1/2">
      <img :src="image" :alt="imageAlt" class="featurette-image-inner" />
    </div>
    <div class="right-featurette-content w-full md:w-1/2">
      <Typography variant="title" class="featurette-title">{{ title }}</Typography>
      <Typography variant="subtitle" class="featurette-subtitle">{{ subtitle }}</Typography>
      <Typography variant="body" class="featurette-description">{{ description }}</Typography>
    </div>
  </div>
</template>

<script>
import Typography from "../elements/Typography";

export default {
  name: 'RightFeaturette',
  components: {
    Typography,
  },
  props: {
    image: {
      type: String,
      required: true,
    },
    imageAlt: {
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
    description: {
      type: String,
      required: true,
    }
  },
};
</script>

<style>
.float-left {
  float: left;
}

.float-right {
  float: right;
}

.featurette {
  padding-top: 120px;
  padding-bottom: 120px;
}

.right-featurette-content {
  text-align: left;
  padding: 0 40px;
}

@media (max-width: 768px) {
  .right-featurette-content {
    text-align: center;
    padding: 0 40px;
  }
}

.featurette-title {
  font-size: min(10vw, 4rem);
  font-weight: 300;
}

.featurette-subtitle {
  font-size: min(5vw, 1.3rem);
}

.featurette-content {
  font-size: min(3vw, 1rem);
}

.featurette-image {
  padding: 0 40px;
}

.featurette-image-inner {
  width: 65%;
  min-width: 300px;
  margin: 0 auto;
}

</style>