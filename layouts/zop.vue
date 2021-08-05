<template>
  <div class="zop-layout">
    <Header />
    <Container>
      <Nuxt />
    </Container>
    <Footer />
  </div>
</template>

<style lang="scss" scoped>
.zop-layout {
  display: grid;
  grid-gap: 6.75rem;
  .container {
    padding-bottom: 6.75rem;
  }
  .footer {
    position: absolute;
    bottom: 0;
    left: 0;
  }
}
</style>
