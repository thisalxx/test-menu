<template>
  <div class="main-menu">
    <div
      v-for="(el, index) in menuList"
      :key="index"
      class="main-menu__item menu-item"
      :class="{'active': el.active}"
      @click="openPage"
    >
      <div
        class="menu-item__icon"
        :style="{backgroundImage: `url(${require('@/assets/menu/'+el.icon+'.png')})`}"
      />
      <div class="menu-item__label">{{ el.label }}</div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'MainMenu',
  data () {
    return {
      menuList: [
        {
          label: 'Лента',
          icon: 'home',
          active: true
        },
        {
          label: 'Мой профиль',
          icon: 'user-circle',
          active: false
        },
        {
          label: 'Соревнования',
          icon: 'flag',
          active: false
        },
        {
          label: 'Эксперты',
          icon: 'monitor',
          active: false
        },
        {
          label: 'Сообщения',
          icon: 'mail',
          active: false
        },
        {
          label: 'Обсуждения',
          icon: 'message-circle',
          active: false
        },
        {
          label: 'Сообщества',
          icon: 'users',
          active: false
        },
        {
          label: 'Люди',
          icon: 'users-alter',
          active: false
        },
        {
          label: 'Аналитика',
          icon: 'trending-up',
          active: false
        },
        {
          label: 'Регламент',
          icon: 'clipboard',
          active: false
        },
        {
          label: 'Документация',
          icon: 'file-text',
          active: false
        },
        {
          label: 'Еще',
          icon: 'arrow-right',
          active: false
        }
      ]
    }
  },
  methods: {
    openPage () {
      this.$emit('openPage')
    }
  }
}
</script>

<style scoped lang="scss">
.main-menu {
  &__item {
    margin-bottom: 8px;
  }
}
.menu-item {
  display: flex;
  align-items: center;
  min-width: 124px;
  height: 24px;
  padding: 0 8px;
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
    width: 16px;
    height: 16px;
    background-position: center center;
    background-repeat: no-repeat;
    background-size: contain;
    flex-shrink: 0;

    img {
      width: 16px;
      height: 16px;
    }
  }

  &__label {
    margin-left: 5px;
    flex-shrink: 0;
  }
}
</style>
