<template>
  <!-- Footer -->
  <!-- Contains an image on the left, and a series of link columns. -->
  <footer class="footer flex flex-wrap place-items-center">
    <div class="content has-text-centered">
      <img :src="logo"
        alt="Logo"
        width="128"
        height="128"
           class="logo"
      />
    </div>
    <div class="flex flex-wrap place-items-center" v-for="(column, id) in columns" :key="id">
      <div class="w-full link-column">
        <Typography variant="h4" class="column-title">{{ column.title }}</Typography>
        <ul >
          <li v-for="(link, linkId) in column.links" :key="linkId">
            <Typography variant="body" class="link">
              <a :href="link.link">{{ link.text }}</a>
            </Typography>
          </li>
        </ul>
      </div>
    </div>
  </footer>
</template>

<script>
import Typography from "../elements/Typography";
export default {
  name: 'Footer',
  components: {Typography},
  props: {
    logo: {
      type: String,
      required: true,
    },
    columns: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped lang="scss">
  .footer {
    background-color: #f5f5f5;
    padding: 40px 0;
    justify-content: space-evenly;
    /* align to top */
    align-items: flex-start;
  }

  .title {
    margin-bottom: 1rem;
    font-weight: 700;
  }

  .link {
    color: #000;
    text-decoration: none;
  }

  .logo {
  }

  .link-column {
    /* Align to top */
    display: flex;
    flex-direction: column;
    justify-content: flex-start;
  }
</style>