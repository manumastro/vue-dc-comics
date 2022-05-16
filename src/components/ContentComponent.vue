<template>
  <div>
    <section id="jumbotron"></section>
    <section id="comics">
      <div class="container d-flex flex-wrap">
        <ComicsCards v-for="(comic, index) in comicsData" :key="`comic-${index}`"
        :comicElement="comic" />
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
    padding: 30px 0 80px 0;
    background-color: #1c1c1c;
  }
</style>