<template>
  <div>
    <Header />
    <div id="app">
      <Terminal msg="Welcome to Your Vue.js App"/>
    </div>
    <Footer />
  </div>
</template>

<script>
import Terminal from './components/Terminal.vue'
import Footer from './components/Footer.vue'
import Header from './components/Header.vue'


export default {
  name: 'App',
  components: {
    Terminal,
    Footer,
    Header
  }
}
</script>

<style>
* {
  margin: 0px;
  padding: 0px;
  background-color: #44494D;
}
</style>
