<template>
  <div id="app">
    <HeaderComponents/>
    <MainComponents/>
  </div>
</template>

<script>
import HeaderComponents from './components/HeaderComponents.vue';
import MainComponents from './components/MainComponents.vue';


export default {
  name: 'App',
  components: {
    HeaderComponents,
    MainComponents
}
}
</script>

<style lang="scss">
@import './assets/style/global.scss'
</style>
