<template>
  <div id="app">
    <Header />
    <router-view/>
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
export default {
    name: 'app',
    components: {
      Header,
      Footer
    }
}
</script>


<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@400&display=swap');
html, body {
  margin: 0px;
  padding: 0px;
}
#app {
  margin: 0;
  padding: 0;
  width: 100vw;
  height: 100vh;
  font-family: 'Roboto', sans-serif;
}
</style>
