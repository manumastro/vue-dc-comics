<template>
  <div>
    <HeaderComponent />
    <ContentComponent />
    <UnderContentComponent />
    <FooterComponent />
  </div>
</template>

<script>
import FooterComponent from './components/FooterComponent.vue'
import HeaderComponent from './components/HeaderComponent.vue'
import ContentComponent from './components/ContentComponent.vue'
import UnderContentComponent from './components/UnderContentComponent.vue'

export default {
  name: 'App',
  components: {
    HeaderComponent,
    FooterComponent,
    ContentComponent,
    UnderContentComponent,
  }
}
</script>

<style lang="scss">
  @import url('https://fonts.googleapis.com/css2?family=Encode+Sans+Condensed:wght@400;500;600&display=swap');
  @import './assets/style/vars'; 
  @import './assets/style/mixins'; 
  @import './assets/style/general'; 
  
</style>
