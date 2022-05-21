<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <NavMenu />
  <SideMenu />
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import NavMenu from './components/NavMenu.vue'
import SideMenu from './components/SideMenu.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    NavMenu,
    SideMenu
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
