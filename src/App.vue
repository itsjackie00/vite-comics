
<template>
  <HeaderComponents />
  <MainComponent />
</template>

<script>
import HeaderComponents from './components/HeaderComponents.vue';
import MainComponent from './components/MainComponent.vue';

  export default {
    name: 'App',
    components: {
      HeaderComponents,
      MainComponent
    }
  }
</script>

<style lang="scss" scoped>

</style>