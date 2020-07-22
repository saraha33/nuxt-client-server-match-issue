<template>
  <button class="hello">
    <!-- @slot create custom content (e.g. icon) left of text -->
    <slot name="left-of-text" />
    <span>{{ text }}</span>
      <!-- @slot create custom content (e.g. icon) right of text -->
    <slot name="right-of-text" />
  </button>
</template>

<script>
export default {
  props: {
    text: {
      type: String,
      default: 'HelloA',
    },
  },
};
</script>
<style lang="scss" scoped>
@import '../styles/variables.scss';
.hello {
  color: $app-color;
}
</style>
