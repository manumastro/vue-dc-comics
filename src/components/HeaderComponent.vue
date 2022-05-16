<template>
  <header class="container">
    <div class="row em-row">
      <div class="col col-left em-col">
        <div class="logo">
          <img src="../assets/img/dc-logo.png" alt="">
        </div>
      </div>
      <div class="col col-right em-col">
        <NavComponent :menuList="list"/>
      </div>
    </div>
  </header>
</template>

<script>
import NavComponent from './NavComponent.vue';
export default {
  name: 'HeaderComponent',
  components: {NavComponent},
  data(){
    return{
      list : 
      [
        {
          name: 'characters',
          isActive: false,
        },
        {
          name: 'comics',
          isActive: true,
        },
        {
          name: 'movies',
          isActive: false,
        },
        {
          name: 'tv',
          isActive: false,
        },
        {
          name: 'games',
          isActive: false,
        },
        {
          name: 'collectibles',
          isActive: false,
        },
        {
          name: 'videos',
          isActive: false,
        },
        {
          name: 'fans',
          isActive: false,
        },
        {
          name: 'news',
          isActive: false,
        },
        {
          name: 'shop',
          isActive: false,
        },
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/_vars.scss';
@import '../assets/style/mixins';

  header{
    height: 125px;
    background-color: white;
    .em-row, .em-col{
      height: 100%;
    }
    .col-left{
      @include center-vertical;
      img{
        height: 80px;
      }
    }
  }
</style>