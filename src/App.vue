<template>
  <NavMenu />
  <SideMenu />
  <DashboardMenu />
</template>

<script>
import NavMenu from './components/NavMenu.vue'
import SideMenu from './components/SideMenu.vue'
import DashboardMenu from './components/DashboardMenu.vue'

export default {
  name: 'App',
  components: {
    NavMenu,
    SideMenu,
    DashboardMenu
  }
}
</script>

<style>
  * {
    margin: 0;
    padding: 0;
  }

  #app {
    height: 84vh;
  }
</style>
