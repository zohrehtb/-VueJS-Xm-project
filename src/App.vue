<template>
  <div id="app">
    <c-header />
    <c-page />
    <c-footer />
  </div>
</template>

<script>
import CHeader from './components/Header/Header.vue'
import CFooter from './components/Footer/Footer.vue'
import CPage from './layouts/index.vue'

export default {
  name: 'App',

  components: {
    CPage,
    CHeader,
    CFooter,
  }
}
</script>

<style lang="scss" src="./assets/scss/Style.scss" />
