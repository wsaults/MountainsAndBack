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

<style scoped lang="scss">
#app {
  display: flex;
  flex-flow: column;
  height: 100%;

  .header {
    flex-shrink: 0;
    margin-top: 0;
  }

  main {
    flex-grow: 1;
    display: flex;
    flex-flow: column;
  }
}
</style>
