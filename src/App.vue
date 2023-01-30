<template>
  <div class="app">
    <MyNavbar></MyNavbar>
    <router-view></router-view>
  </div>
</template>

<script>
import MyNavbar from './components/UI/MyNavbar.vue';

export default {
  components: { MyNavbar }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {
  padding: 20px;
}
</style>