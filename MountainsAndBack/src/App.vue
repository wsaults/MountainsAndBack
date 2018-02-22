<template>
  <div id="app">
    <header-container class="header"></header-container>
    <main>
      <router-view/>
    </main>
    <!-- <footer-container class="footer"></footer-container> -->
  </div>
</template>

<script>
import Header from './components/Header.vue'

export default {
  name: 'App',
  components: {
    'header-container': Header
  }
}
</script>

<style style scoped lang="scss">
#app {
  display: flex;
  flex-flow: column;
  min-height: 100vh;

  .header {
    flex-shrink: 0;
  }

  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
