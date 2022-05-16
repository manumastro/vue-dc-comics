<template>
  <div>
    <section id="jumbotron"></section>
    <section id="comics">
      <div class="container d-flex flex-wrap">
        <div class="comic-card d-flex justify-content-center align-items-start"
        v-for="(comic, index) in comicsData" :key="`comic-${index}`"
        >
          <a class="d-flex justify-content-center align-items-center flex-column" href="#">
            <img :src="comic.thumb" :alt="comic.series">
            <span>{{comic.series}}</span>
          </a>
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
    .comic-card{
      width: calc(100% / 6);
      margin: 20px 0;
      a{
        text-decoration: none;  
        span{
          align-self: flex-start;
          text-transform: uppercase;
          color: white;
          width: 185px;
        }
        img{
          width: 185px;
          height: 185px;
          object-fit: cover;
          object-position: 100% 0;
          margin-bottom: 15px;
        }
      }
      
    }
  }
</style>