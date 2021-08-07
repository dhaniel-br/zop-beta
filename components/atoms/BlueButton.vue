<template>
  <div>
    <NuxtLink to="/z/upload">
      <button class="button">
        <!-- eslint-disable-next-line vue/no-v-html -->
        <div v-html="$feathericons['plus'].toSvg()"></div>
        <p>Postar um meme</p>
      </button>
    </NuxtLink>
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
  background: color(zop);
  color: color(white, 'lighter');
  gap: 12px;
  cursor: pointer;

  border-radius: 16px;

  p {
    font-weight: 600;
  }
  &:hover {
    background: rgba(83, 112, 254, 0.8);
  }
}
</style>
