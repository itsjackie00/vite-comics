
<template>
  <div class="main-container">
    <HeaderComponents />
  <Jumbotron />
  <MainComponent />
  <FooterComponentTop />
  <FooterComponentMiddle />
  <FooterComponentBottom />
  </div>
  
</template>

<script>
import HeaderComponents from './components/HeaderComponents.vue';
import Jumbotron from './components/Jumbotron.vue';
import MainComponent from './components/MainComponent.vue';
import FooterComponentTop from './components/FooterComponentTop.vue';
import FooterComponentMiddle from './components/FooterComponentMiddle.vue';
import FooterComponentBottom from './components/FooterComponentBottom.vue';

  export default {
    name: 'App',
    components: {
      HeaderComponents,
      Jumbotron,
      MainComponent,
      FooterComponentTop,
      FooterComponentMiddle,
      FooterComponentBottom
    }
  }
</script>

<style lang="scss" scoped>
.main-container{
  width: 100%;
}
</style>