<template>
  <header class="header">
    <Container>
      <NuxtLink to="/">
        <Logo />
      </NuxtLink>

      <ul class="items">
        <li class="item">
          <NuxtLink class="item" to="/">
            <!-- eslint-disable-next-line vue/no-v-html -->
            <div v-html="$feathericons['home'].toSvg()"></div>
          </NuxtLink>
        </li>
        <li>
          <NuxtLink class="item" to="/z/profile">
            <!-- eslint-disable-next-line vue/no-v-html -->
            <div v-html="$feathericons['user'].toSvg()"></div>
          </NuxtLink>
        </li>
      </ul>
    </Container>
  </header>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({})
</script>

<style lang="scss" scoped>
.header {
  width: 100%;
  height: 110px;
  background: color(black, 'dark');
  @include screen('small') {
    display: grid;
    justify-content: center;
  }
  .container {
    display: grid;
    height: 100%;
    grid-auto-flow: column;
    justify-content: space-between;
    align-items: center;
    @include screen('medium') {
      display: grid;
      height: 100%;
      grid-auto-flow: row;
      justify-content: space-between;
      align-items: center;
    }
    .items {
      display: grid;
      height: 100%;
      grid-auto-flow: column;
      justify-content: center;
      align-items: center;
      grid-gap: 32px;
      .item {
        display: grid;
        justify-content: center;
        align-items: center;
        width: 48px;
        height: 48px;
        color: color(zop);
        &:hover {
          background: color(black, 'light');
          border-radius: 8px;
        }
        &.nuxt-link-exact-active {
          border-bottom: 2px solid color(zop, 'base');
          &:hover {
            background: color(black, 'dark');
            border-radius: 0px;
          }
        }
      }
    }
  }
}
</style>
