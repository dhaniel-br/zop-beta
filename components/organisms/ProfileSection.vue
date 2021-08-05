<template>
  <div class="profile-header">
    <Container>
      <ProfileHeader />
      <div class="buttons">
        <BlueButton />
        <RedButton />
      </div>
    </Container>
  </div>
</template>

<style lang="scss" scoped>
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  gap: 64px;
  .buttons {
    display: flex;
    flex-flow: column;
    justify-content: space-between;
    align-items: center;
    grid-gap: 32px;
  }
}
</style>
