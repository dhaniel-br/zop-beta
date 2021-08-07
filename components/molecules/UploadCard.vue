<template>
  <Container>
    <iframe
      src="https://docs.google.com/forms/d/e/1FAIpQLSdt3QzWsbyQS3Xevd9i3OgdzjqFc-ZUYS8JvhgaTKtd8qRobw/viewform?"
      frameborder="0"
      class="upload-form"
    ></iframe>
  </Container>
</template>

<script lang="ts">
import Vue from 'vue'
export default Vue.extend({})
</script>

<style lang="scss" scoped>
.container {
  display: grid;
  justify-content: center;
  .upload-form {
    width: 700px;
    height: 520px;
    border-radius: 16px;
    @include screen('medium') {
      width: 375px;
      height: 520px;
    }
  }
}
</style>
