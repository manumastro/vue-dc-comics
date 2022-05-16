<template>
  <header class="container">
    <div class="row em-row">
      <div class="col col-left em-col">
        <div class="logo">
          <img src="../assets/img/dc-logo.png" alt="">
        </div>
      </div>
      <div class="col col-right em-col">
        <nav>
          <ul>
            <li v-for="(el, index) in list" :key="`menu${index}`">
              <a
              :class="{ active : el.isActive }" 
              href="#">{{el.name}}</a>
            </li>
            <!-- <li><a class="active" href="#">comics</a></li>
            <li><a href="#">movies</a></li>
            <li><a href="#">tv</a></li>
            <li><a href="#">games</a></li>
            <li><a href="#">collectibles</a></li>
            <li><a href="#">videos</a></li>
            <li><a href="#">fans</a></li>
            <li><a href="#">news</a></li>
            <li><a href="#">shop</a></li> -->
          </ul>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'HeaderComponent',
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
    nav{
      @include center;
      height: 100%;
      ul{
        display: flex;
        text-transform: uppercase;
        list-style: none;
        margin: auto;
        a{
          color: black;
          text-decoration: none;
          font-size: 13px;
          font-weight: 600;
          margin-right: 30px;
        }
        .active{
          position: relative;
          color: $primary-color;
          &:before{
            position: absolute;
            content: '';
            bottom: -54px;
            right: 0;
            width: 100%;
            border-bottom: 5px solid $primary-color;
          }
        }
        
      }
    }
    
      
  
  }
</style>