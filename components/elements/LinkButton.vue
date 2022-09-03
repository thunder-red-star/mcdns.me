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
      <svg class="hover-arrow" width="10" height="10" viewBox="0 0 10 10" aria-hidden="true">
        <g fill-rule="evenodd">
          <path class="hover-arrow-line-path" d="M0 5h7"></path>
          <path class="hover-arrow-tip-path" d="M1 1l4 4-4 4"></path>
        </g>
      </svg>

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

  /* Make the border radius half the element height */
  border-radius: 50vh;
  padding: 0.15rem 0.7rem;
  font-weight: 600;
  cursor: pointer;
  font-family: Inter, sans-serif;
  font-size: 0.9rem;
  transition: all 0.2s ease-in-out;


  &:hover {
    --hover-displace: 2px;
    --hover-opacity: 1;
  }

  &:active {
    transform: translateY(2px);
  }

  &:disabled {
    opacity: 0.5;
    cursor: not-allowed;
  }
}

.hover-arrow-tip-path {
  stroke: #1a1a1a;
  stroke-width: 2;
  fill: none;
  margin-left: 0.5rem;
  transform: translateX(var(--hover-displace, 0));
  transition: transform 0.2s ease-in-out;
}

.hover-arrow-line-path {
  stroke: #1a1a1a;
  stroke-width: 2;
  fill: none;
  opacity: var(--hover-opacity, 0);
  transition: opacity 0.2s ease-in-out;
}

.hover-arrow {
  display: inline-block;
  vertical-align: middle;
  transform: translateX(var(--hover-displace, 0)) translateY(-0.5px);
  transition: transform 0.2s ease-in-out;
}
</style>