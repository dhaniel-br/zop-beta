<template>
  <div>
    <h2 class="ztag-title"><span class="z">z/</span> {{ tag }}</h2>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: {
    tag: {
      type: String,
      required: true
    }
  }
})
</script>

<style lang="scss" scoped>
.ztag-title {
  color: color(white, 'lighter');
  font-weight: 600;
  span {
    color: color(zop);
  }
}
</style>
