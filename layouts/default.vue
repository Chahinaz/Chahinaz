<template>
  <div>
    <Menu/>
    <div v-if="isHomePage"><Header/></div>
    <nuxt/>
    <div><Footer/></div>
  </div>
</template>

<script>
import Menu from '../components/header/Menu.vue'
import Header from '../components/header/Header.vue'
import Footer from '../components/Footer.vue'

export default {
  components: {
    Menu,
    Header,
    Footer
  },
  data() {
    return {
      isHomePage: this.$router.history.current.fullPath === "/" || ""
    }
  }
}
</script>

<style>
html {
  font-family: "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  font-size: 16px;
  word-spacing: 1px;
  -ms-text-size-adjust: 100%;
  -webkit-text-size-adjust: 100%;
  -moz-osx-font-smoothing: grayscale;
  -webkit-font-smoothing: antialiased;
  box-sizing: border-box;
}

*, *:before, *:after {
  box-sizing: border-box;
  margin: 0;
}
</style>
