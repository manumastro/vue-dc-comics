<template>
  <div>
    <HeaderComponent />
    <MainComponent />
    <FooterComponent />
  </div>
</template>

<script>
import FooterComponent from './components/FooterComponent.vue'
import MainComponent from './components/MainComponent.vue'
import HeaderComponent from './components/HeaderComponent.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    MainComponent,
    FooterComponent,
  }
}
</script>

<style lang="scss">
  @import './assets/style/vars'; 
  @import './assets/style/mixins'; 
  @import './assets/style/general'; 
</style>
