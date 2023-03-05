<template>
  <div id="app">
    <div class="page" :class="{'opened-sub-menu': isOpenSubMenu}">
      <div class="side">
        <div class="side__main-menu">
          <LogoType />
          <CreateBtn />
          <MainMenu @openPage="isOpenSubMenu = !isOpenSubMenu" />
          <SocialLinks />
        </div>
        <div class="side__sub-menu">
          <SubMenu />
        </div>
      </div>
      <div class="content">
        page content
      </div>
    </div>
  </div>
</template>

<script>

import LogoType from '@/components/LogoType.vue'
import CreateBtn from '@/components/CreateBtn.vue'
import MainMenu from '@/components/MainMenu.vue'
import SubMenu from '@/components/SubMenu.vue'
import SocialLinks from '@/components/SocialLinks.vue'

export default {
  name: 'App',
  components: {
    SocialLinks,
    SubMenu,
    MainMenu,
    CreateBtn,
    LogoType
  },
  data () {
    return {
      isOpenSubMenu: false
    }
  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@300;400&display=swap');
* {
  box-sizing: border-box;
}
html,body,#app,.page,.sub-menu {
  height: 100%;
}
html, body {
  font-family: 'Roboto', sans-serif;
  font-size: 12px;
}
body {
  margin: 0;
}
.page {
  width: 100%;
  display: flex;
}
.side {
  display: flex;
  flex-shrink: 0;

  &__main-menu {
    width: 156px;
    padding: 16px;
    transition: all .3s ease;

    > div + div {
      margin-top: 16px;
    }
  }

  &__sub-menu {
    width: 158px;
    padding: 16px;
    border-left: 1px solid #eee;
    background-color: #fff;
    box-shadow: 0 0 5px #eee;
    position: absolute;
    left: 156px;
    top: 0;
    bottom: 0;
    z-index: 1;
    transition: all .3s ease;
  }
}
.content {
  width: 100%;
  padding: 16px;
  border-left: 1px solid #eee;
  background-color: #fff;
  z-index: 2;
  transition: all .3s ease;
}
.opened-sub-menu {
  .content {
    margin-left: 158px;
  }
  .side__main-menu {
    width: 64px;
  }
  .side__sub-menu {
    box-shadow: none;
    left: 64px;
  }
  .logo__text {
    display: none;
  }
  .create-btn {
    min-width: auto;
    width: 32px;
    height: 32px;
    padding: 0;
    justify-content: center;

    &__label {
      display: none;
    }
  }
  .main-menu {
    .menu-item {
      width: 32px;
      min-width: auto;
      height: 32px;
      &__label {
        display: none;
      }
    }
  }
  .social-links {
    justify-content: center;

    > div + div {
      margin-top: 8px;
    }
  }
}
</style>
