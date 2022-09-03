<template>
  <!-- Button template -->
  <!-- A button is a clickable element that performs an action. -->
  <!-- Button types:
    - 1, Primary
    - 2, Secondary
    - 3, Success
    - 4, Danger
    - 5, Warning
    - 6, Info
    - 7, Link
  -->
  <button
    class="button"
    v-bind:class="'is-link'"
    @click="open(link)"
    v-bind:disabled="disabled"
  >
    {{ text }}
  </button>
</template>

<script>
export default {
  name: 'LinkButton',
  props: {
    text: {
      type: String,
      required: true,
    },
    disabled: {
      type: Boolean,
      required: false,
      default: false,
    },
    link: {
      type: String,
      required: false,
      default: '',
    },
    onClick: {
      type: Function,
      required: false,
      default: () => {
        return true;
      },
    },
  },
  methods: {
    click() {
      this.$emit('click');
    },
    open(link) {
      window.open(link, '_blank');
    }
  },
  mounted() {
    return true;
  },
};
</script>

<style scoped lang="scss">
  .button {
    border: 2px solid #1a1a1a;
    border-radius: 10px;
    padding: 0.5rem 1rem;
    font-weight: 600;
    cursor: pointer;
    font-size: max(min(5vw, 1.25rem), 1rem);
    transition: all 0.2s ease-in-out;
    &:hover {
      transform: translateY(-2px);
    }
    &:active {
      transform: translateY(2px);
    }
    &:disabled {
      opacity: 0.5;
      cursor: not-allowed;
    }
  }
</style>