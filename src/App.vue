<template>
  <div id="app">
    <HeaderComponent />
    <MainComponent />
    <PanelImages />
    <FooterComponent />
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import PanelImages from './components/PanelImages.vue';
import FooterComponent from './components/FooterComponent.vue';

export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent,
    PanelImages,
    FooterComponent,
    
}
}
</script>

<style lang="scss">
@import '@/assets/style/general';

#app {
  h1{
    margin-bottom: 0;
    line-height: 2.5;
  }

}
</style>
