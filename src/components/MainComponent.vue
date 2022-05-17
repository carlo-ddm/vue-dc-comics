<template>
  <main>
    <ContentComponent />
  </main>
</template>

<script>
import ContentComponent from './ContentComponent.vue';

export default {
  name: 'MainComponent',
  components: {
    ContentComponent,
  }
}
</script>

<style lang="scss" scoped>
  main {
    background-color: black;
  }
</style>