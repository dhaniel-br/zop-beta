<template>
  <div class="container">
    <slot />
  </div>
</template>
<style lang="scss" scoped>
.container {
  margin: 0 auto;
  max-width: 960px;
  @include screen('small') {
    width: 90%;
  }
  @include screen('medium') {
    width: 85%;
  }
  @include screen('large') {
    width: 70%;
  }
  @include screen('infinity') {
    width: 70%;
  }
}
</style>
