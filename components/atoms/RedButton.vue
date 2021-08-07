<template>
  <div>
    <button class="button">
      <!-- eslint-disable-next-line vue/no-v-html -->
      <div v-html="$feathericons['lock'].toSvg()"></div>
      <p>Login será disponibilizado em breve</p>
    </button>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" scoped>
.button {
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 20px 44px;

  /* zop/base */
  background: #f12547;
  color: color(white, 'lighter');
  gap: 12px;
  cursor: pointer;

  border-radius: 16px;

  p {
    font-weight: 600;
  }
  &:hover {
    background: rgba(241, 37, 71, 0.8);
  }
}
</style>
