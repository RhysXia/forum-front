<template lang="pug">
  header.header
    .nav-wrapper
        .nav
            nuxt-link.logo(to="/") Rhys
            ul.nav-menu
                li
                    nuxt-link.menu(to="/a") 菜单1
                li
                    nuxt-link.menu(to="/a") 菜单1
            ul.nav-menu.right
                li
                    nuxt-link.menu(to="/signIn") 登录
                li
                    nuxt-link.menu(to="/signUp") 注册
</template>
<script>
export default {}
</script>
<style lang="scss" scoped>
@import '@/assets/styles/variables.scss';
.header {
  height: $--header-height;
  .nav-wrapper {
    z-index: 1;
    width: 100%;
    height: $--header-height;
    background-color: hsla(0, 0%, 100%, 0.4);
    box-shadow: 0 1px 2px rgba(0, 0, 0, 0.1);
    position: fixed;
    .nav {
      width: $--header-width;
      margin: 0 auto;
      height: $--header-height;
      display: flex;
      align-items: center;
      .logo {
        font-size: 2em;
        text-decoration: none;
        font-weight: bold;
        color: $--color-primary;
      }
      .nav-menu {
        margin: 0 0 0 1.5em;
        padding: 0;
        list-style: none;
        li {
          float: left;
        }
        .menu {
          display: block;
          height: $--header-height;
          line-height: $--header-height;
          padding: 0 1em;
          text-decoration: none;
          color: $--color-text;
          transition: background-color $--transition-time * 2 ease;
          &:hover,
          &.nuxt-link-active {
              background-color: hsla(0,0%,100%,.5);
          }
        }
        &.right{
            margin: 0 0 0 auto;
        }
      }
    }
  }
}
</style>
