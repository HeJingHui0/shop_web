<template>
  <div id="app">
    <router-view></router-view>
    <tabbar v-show="$route.meta.showTabbar"></tabbar>
  </div>
</template>

<script>
import Tabbar from './components/Tabbar/Tabbar'
export default {
  name: 'App',
  components: {
    Tabbar
  },
  mounted() {
    this.$store.dispatch('getUserInfo')
  }
}
</script>

<style scoped>
#app {
  width: 100%;
  height: 100%;
  background-color: #fff;
}
</style>
