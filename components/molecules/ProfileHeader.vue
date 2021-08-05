<template>
  <Container>
    <div class="profile-header">
      <Avatar />
      <Ztag tag="bifotepadrao" />
      <Description text="descrição 🇧🇷🇧🇷🇧🇷🇧🇷🇧🇷🇧🇷🇧🇷" />
    </div>
  </Container>
</template>

<style lang="scss" scoped>
.container {
  display: grid;
  justify-content: center;
  .profile-header {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    gap: 32px;

    position: static;
    width: 496px;
    height: 304px;
    left: 0px;
    top: 0px;

    .logo {
      width: 120px;
      height: 120px;
    }
    .ztag-title {
      text-align: center;
    }
  }
}
</style>
