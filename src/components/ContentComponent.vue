<template>
  <div>
    <section id="jumbotron"></section>
    <section id="comics">
      <div class="container" id="current-series">
        <span>current series</span>
      </div>
      <div class="container d-flex flex-wrap">
        <ComicsCards v-for="(comic, index) in comicsData" :key="`comic-${index}`"
        :comicElement="comic" />
      </div>
      <div class="load-more">
        <a href="#"><button>load more</button></a>
      </div>
    </section>
  </div>
</template>

<script>
import comics from '../assets/data/dc-comics.json';
import ComicsCards from './ComicsCards.vue';
export default {
  components: { ComicsCards },
  name: 'ContentComponent',
  data(){
    return{
      comicsData: comics,
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/_mixins.scss';
@import '../assets/style/_vars.scss';
  #jumbotron{
    background-image: url('../assets/img/jumbotron.jpg');
    padding: 21vh 0;
  }
  #comics{
    position: relative;
    padding: 30px 0 0 0;
    background-color: #1c1c1c;
    #current-series span{
      position: absolute;
      top: -32px;
      left: 310px;
      padding: 5px 25px;
      font-size: 28px;
      font-weight: bold;
      text-transform: uppercase;
      color: whitesmoke;
      background-color: $primary-color;
    }
    .load-more{
      text-align: center;
      padding: 20px 0;
      button{
        color: whitesmoke;
        text-transform: uppercase;
        background-color: $primary-color;
        padding: 8px 60px;
        font-size: 12px;
        font-weight: bold;
        border: none;
      }
    }
  }
</style>