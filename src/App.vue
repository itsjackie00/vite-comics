
<template>
  <HeaderComponents />
  <MainComponent />
  <FooterComponentTop />
  <FooterComponentMiddle />
</template>

<script>
import HeaderComponents from './components/HeaderComponents.vue';
import MainComponent from './components/MainComponent.vue';
import FooterComponentTop from './components/FooterComponentTop.vue';
import FooterComponentMiddle from './components/FooterComponentMiddle.vue';

  export default {
    name: 'App',
    components: {
      HeaderComponents,
      MainComponent,
      FooterComponentTop,
      FooterComponentMiddle
    }
  }
</script>

<style lang="scss" scoped>

</style>