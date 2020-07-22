<template>
  <div class="container">
    <HelloA>
      <template v-slot:right-of-text>
      </template>
      <template v-slot:left-of-text>
      </template>
    </HelloA>
  </div>
</template>

<!--
THIS IS OK:
<template>
  <div class="container">
    <HelloA>
      <template v-slot:right-of-text>
        test
      </template>
      <template v-slot:left-of-text>
        test
      </template>
    </HelloA>
  </div>
</template>
-->

<!--
THIS IS NOT OK:
<template>
  <div class="container">
    <HelloA>
      <template v-slot:right-of-text>
        <div>test</div>
      </template>
      <template v-slot:left-of-text>
        <div>test</div>
      </template>
    </HelloA>
  </div>
</template>
-->

<script>
import { HelloA } from '../components/vue-package-test-x';

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
