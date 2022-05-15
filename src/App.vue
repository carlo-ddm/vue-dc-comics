<template>
  <div id="app">
    <header-component />
    <main-component />
    <icons-items />
    <footer-component />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import IconsItems from './components/IconsItems.vue';
import FooterComponent from './components/FooterComponent.vue';



export default {
  name: 'App',
  components: {
   HeaderComponent,
   MainComponent,
   IconsItems,
   FooterComponent,
  }
}
</script>

<style lang="scss">
@import './assets/styles/vars';
@import './assets/styles/general';
@import './assets/styles/utilities';



</style>
