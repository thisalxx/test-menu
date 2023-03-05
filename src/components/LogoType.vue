<template>
  <div class="logo">
    <div class="logo__icon">
      <img src="../assets/logo-icon.png" alt="">
    </div>
    <div class="logo__text">
      <img src="../assets/logo-text.png" alt="">
    </div>
  </div>
</template>

<script>
export default {
  name: 'LogoType'
}
</script>

<style scoped lang="scss">
.logo {
  display: flex;
  align-items: center;

  &__icon {
    width: 32px;
    height: 32px;
    text-align: center;
    flex-shrink: 0;
  }

  &__text {
    margin-top: -5px;
    margin-left: 10px;
  }
}
</style>
