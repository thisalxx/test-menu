<template>
  <div class="create-btn">
    <div class="create-btn__label">Создать</div>
    <div class="create-btn__icon">+</div>
  </div>
</template>

<script>
export default {
  name: 'CreateBtn'
}
</script>

<style scoped lang="scss">
.create-btn {
  display: flex;
  align-items: center;
  justify-content: space-between;
  min-width: 124px;
  height: 28px;
  padding: 0 14px;
  border-radius: 8px;
  box-shadow: 0 4px 4px rgba(0,0,0,.25);
  background-color: #2378E9;
  color: #fff;
  cursor: pointer;

  &:hover {
    background-color: #213464;
  }

  &__icon {
    font-size: 23px;
  }

  &__label {
    margin-left: 14px;
  }
}
</style>
