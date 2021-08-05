<template>
  <div class="description">
    <p class="text">{{ text }}</p>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
  props: {
    text: {
      type: String,
      required: true
    }
  }
})
</script>

<style lang="scss" scoped>
.description {
  color: color(white, 'light');
}
</style>
