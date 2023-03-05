<template>
  <div class="sub-menu">
    <div
      v-for="(el, index) in menuList"
      :key="index"
      class="sub-menu__item menu-item"
      :class="{'active': el.active}"
    >
      <div
        class="menu-item__icon"
        :style="{backgroundImage: `url(${require('@/assets/sub-menu/'+el.icon+'.png')})`}"
      />
      <div class="menu-item__label">{{ el.label }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SubMenu',
  data () {
    return {
      menuList: [
        {
          label: 'О событии',
          icon: 'stat',
          active: true
        },
        {
          label: 'Задачи',
          icon: 'case',
          active: false
        },
        {
          label: 'Все участники',
          icon: 'users',
          active: false
        },
        {
          label: 'Рейтинг',
          icon: 'cup',
          active: false
        },
        {
          label: 'Моя анкета',
          icon: 'user',
          active: false
        },
        {
          label: 'Правила',
          icon: 'document',
          active: false
        },
        {
          label: 'Информация для участника',
          icon: 'book',
          active: false
        },
        {
          label: 'Мой сертификат',
          icon: 'medal',
          active: false
        },
        {
          label: 'Обратная связь',
          icon: 'phone',
          active: false
        },
        {
          label: 'FAQ',
          icon: 'info',
          active: false
        }
      ]
    }
  }
}
</script>

<style scoped lang="scss">
.sub-menu {
  &__item {
    margin-bottom: 8px;
  }
}
.menu-item {
  display: flex;
  align-items: center;
  min-width: 124px;
  height: 32px;
  padding: 0 0 0 4px;
  border-radius: 8px;
  border: 1px solid transparent;
  color: #213464;
  cursor: pointer;

  &:hover {
    background-color: #eee;
  }

  &.active {
    border-color: #eee;
  }

  &__icon {
    width: 24px;
    height: 24px;
    background-position: center center;
    background-repeat: no-repeat;
    background-size: contain;
    flex-shrink: 0;
  }

  &__label {
    margin-left: 5px;
  }
}
</style>
