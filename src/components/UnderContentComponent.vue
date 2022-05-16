<template>
  <section>
    <div class="container em-container">
      <ul>
        <!-- <li v-for="(el, index) in list" :key="`element${index}`">
          <a href="#">
            <img :src="el.image" :alt="el.name">
            <span>{{el.name}}</span>
          </a>
        </li> -->
        <UnderContentCards v-for="(item, index) in list" :key="`item-${index}`"
        :card = "item"
        />
      </ul>
    </div>
  </section>
</template>

<script>
import UnderContentCards from './UnderContentCards.vue'
export default {
  components: { UnderContentCards },
  name: 'UnderContentComponent',
  data(){
    return{
      list: 
        [
          {
            image: require('../assets/img/buy-comics-digital-comics.png'),
            name: 'digital comics',
          },
          {
            image: require('../assets/img/buy-comics-merchandise.png'),
            name: 'dc merchandise',
          },
          {
            image: require('../assets/img/buy-comics-subscriptions.png'),
            name: 'subscription',
          },
          {
            image: require('../assets/img/buy-comics-shop-locator.png'),
            name: 'comic shop locator',
          },
          {
            image: require('../assets/img/buy-dc-power-visa.svg'),
            name: 'dc power visa',
          },
        ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/_vars.scss';
@import '../assets/style/_mixins.scss';
section{
  //height: 150px;
  padding: 50px 0;
  background-color: $primary-color;
  .em-container{
    height: 100%;
  ul{
    height: 100%;
    margin: auto;
    list-style: none;
    @include center;
    justify-content: space-between;
    
  }
  }
  
}
</style>