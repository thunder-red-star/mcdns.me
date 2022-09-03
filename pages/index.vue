<template>
  <div>
    <LeftFeaturette
      :image="downloading"
      :image-alt="'Featurette 1'"
      :title="'Featurette 1'"
      :subtitle="'It\'ll blow your mind.'"
      :description="'Featurette 1 description'"
    />
    <RightFeaturette
      :image="fileTransfer"
      :image-alt="'Featurette 2'"
      :title="'Featurette 2'"
      :subtitle="'How cool is that?'"
      :description="'Featurette 2 description'"
    />
    <Hero
        :background-image="interiorDesign"
        :title="'Get this application'"
        :subtitle="'And get ready to be blown away'"
        :button-text="'Learn More'"
        :button-link="'https://google.com'"
    />
  </div>
</template>

<script>
import Hero from '@/components/blocks/Hero.vue';
import LeftFeaturette from '@/components/blocks/LeftFeaturette';
import RightFeaturette from "../components/blocks/RightFeaturette";

import serverStands from '~/assets/images/background/server-stands.jpg';
import interiorDesign from '~/assets/images/background/interior-design.jpg';
import fileTransfer from '~/assets/vectors/clip-file-transfer.svg';
import downloading from '~/assets/vectors/clip-downloading.svg';
export default {
  name: 'Home',
  components: {
    RightFeaturette,
    LeftFeaturette,
    Hero,
  },
  data() {
    return {
      serverStands,
      fileTransfer,
      downloading,
      interiorDesign,
    };
  },
};
</script>

<style>
</style>