<template>
  <div id="app">
    <Navbar/>
    <router-view/>
    <Footer/>
  </div>
</template>

<script>
// Import Navbar
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'

export default {
  name: 'app',
  components: { 
    Navbar,
    Footer
  },
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  overflow-x: hidden;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}

.breadcrumb {
  padding: 10px !important;
  font-size: 12px;
}
</style>
