<template>
  <div class="container">
    <HelloA />
  </div>
</template>

<script>
import { HelloA } from 'vue-package-test-x';

export default {
  components: {
    HelloA,
  },
};
</script>

<style>
.container {
  margin: 0 auto;
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
}
</style>
