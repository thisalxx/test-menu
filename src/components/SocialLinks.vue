<template>
  <div class="social-links">
    <div class="social-links__link telegram"></div>
    <div class="social-links__link linkedin"></div>
    <div class="social-links__link habr"></div>
    <div class="social-links__link git"></div>
  </div>
</template>

<script>
export default {
  name: 'SocialLinks'
}
</script>

<style scoped lang="scss">
.social-links {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;

  &__link {
    width: 20px;
    height: 20px;
    border-radius: 4px;
    background-color: #2378E9;
    background-position: center center;
    background-repeat: no-repeat;
    cursor: pointer;

    &:hover {
      background-color: #213464;
    }
  }
  .telegram {
    background-image: url('@/assets/social/telegram.png');
  }
  .linkedin {
    background-image: url('@/assets/social/linkedin.png');
  }
  .habr {
    background-image: url('@/assets/social/habr.png');
  }
  .git {
    background-image: url('@/assets/social/git.png');
  }
}
</style>
