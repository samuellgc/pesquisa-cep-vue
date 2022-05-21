<template>
  <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <NavMenu />
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import NavMenu from './components/NavMenu.vue'

export default {
  name: 'App',
  components: {
    // HelloWorld
    NavMenu
  }
}
</script>

<style>
  * {
    margin: 0;
    padding: 0;
  }
</style>
