
<template>
  <HeaderComponents />
  <MainComponent />
  <FooterComponentTop />
</template>

<script>
import HeaderComponents from './components/HeaderComponents.vue';
import MainComponent from './components/MainComponent.vue';
import FooterComponentTop from './components/FooterComponentTop.vue';

  export default {
    name: 'App',
    components: {
      HeaderComponents,
      MainComponent,
      FooterComponentTop
    }
  }
</script>

<style lang="scss" scoped>

</style>