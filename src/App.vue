<template>
  <div id="app">
    <HeaderComponent />
    <MainComponent />
    <PanelImages />
    <FooterComponent />
    <BottomFooter />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import PanelImages from './components/PanelImages.vue';
import FooterComponent from './components/FooterComponent.vue';
import BottomFooter from './components/BottomFooter.vue';


export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent,
    PanelImages,
    FooterComponent,
    BottomFooter
}
}
</script>

<style lang="scss">
@import '@/assets/style/general';

#app {
  height: 100vh;
  
  h1{
    margin-bottom: 0;
    line-height: 2.5;
  }

}
</style>
