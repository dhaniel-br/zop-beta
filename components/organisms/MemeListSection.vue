<template>
  <div class="meme-list-section">
    <Container>
      <nav>
        <ul class="items">
          <li class="item">0 Memez</li>
          <li class="item">0 Zipados</li>
          <li class="item">0 Zipandos</li>
        </ul>
      </nav>
    </Container>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({})
</script>

<style lang="scss" scoped>
.meme-list-section {
  .container {
    display: flex;
    height: 100%;
    flex-flow: column;
    justify-content: space-between;
    align-items: center;
    .items {
      display: grid;
      height: 100%;
      grid-auto-flow: column;
      justify-content: center;
      align-items: center;
      margin-top: 64px;
      grid-gap: 32px;
      @include screen('small') {
        grid-auto-flow: row;
        grid-gap: 4px;
      }
      .item {
        display: grid;
        justify-content: center;
        align-items: center;
        width: 190px;
        height: 72px;
        color: color(white, 'lighter');
      }
    }
  }
}
</style>
