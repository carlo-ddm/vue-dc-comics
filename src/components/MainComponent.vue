<template>
  <main>
    <div class="container">
      <ContentComponent />
      <IconsItems />
    </div>
  </main>
</template>

<script>
import ContentComponent from './ContentComponent.vue';
import IconsItems from './IconsItems.vue'

export default {
  name: 'MainComponent',
  components: {
    ContentComponent,
    IconsItems,
  }
}
</script>

<style lang="scss" scope>

</style>