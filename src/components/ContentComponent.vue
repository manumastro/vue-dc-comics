<template>
  <div>
    <section id="jumbotron"></section>
    <section id="comics">
      <div class="container">
        <div class="comic-card"
        v-for="(comic, index) in comicsData" :key="`comic-${index}`"
        >
        <span>{{comic.series}}</span>
        </div>
      </div>
    </section>
  </div>
</template>

<script>
import comics from '../assets/data/dc-comics.json';
export default {
  name: 'ContentComponent',
  data(){
    return{
      comicsData: comics
    }
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/_mixins.scss';
  #jumbotron{
    background-image: url('../assets/img/jumbotron.jpg');
    padding: 21vh 0;
  }
  #comics{
    background-color: #1c1c1c;
  }
</style>