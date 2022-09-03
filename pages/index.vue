<template>
  <div>
    <LeftFeaturette
      :image="downloading"
      :image-alt="'Featurette 1'"
      :title="'Featurette 1'"
      :subtitle="'It\'ll blow your mind.'"
      :description="'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.\n'+
'\n'"
    />
    <RightFeaturette
      :image="fileTransfer"
      :image-alt="'Featurette 2'"
      :title="'Featurette 2'"
      :subtitle="'How cool is that?'"
      :description="'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.\n'+
'\n'"
    />
    <Hero
        :background-image="interiorDesign"
        :title="'Get this application'"
        :subtitle="'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.\n'+
'\n'"
        :button-text="'Learn More'"
        :button-link="'https://google.com'"
    />
    <Footer
      :logo="logo"
      :columns="columns"
    />
  </div>
</template>

<script>
import Hero from '@/components/blocks/Hero.vue';
import LeftFeaturette from '@/components/blocks/LeftFeaturette';
import RightFeaturette from "@/components/blocks/RightFeaturette";
import Footer from "@/components/blocks/Footer";

import serverStands from '~/assets/images/background/server-stands.jpg';
import interiorDesign from '~/assets/images/background/interior-design.jpg';
import fileTransfer from '~/assets/vectors/clip-file-transfer.svg';
import downloading from '~/assets/vectors/clip-downloading.svg';

import logo from '~/assets/branding/logo.svg';
import links from '~/data/links.json';

import interCSS from '~/assets/css/font-inter.css';

export default {
  name: 'Home',
  components: {
    Footer,
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
      logo,
      columns: links,
      interCSS,
    };
  },
};
</script>

<style>
</style>