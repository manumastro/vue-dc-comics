<template>
  <div class="d-flex justify-content-center align-items-start">
    <a class="d-flex justify-content-center align-items-center flex-column" href="#">
      <img :src="comicElement.thumb" :alt="comicElement.series">
      <span>{{comicElement.series}}</span>
    </a>
  </div>
</template>

<script>
export default {
  name: 'ComicsCards',
  props: {
    comicElement: Object,
  }
}

</script>

<style lang="scss" scoped>
@import '../assets/style/_mixins.scss';
@import '../assets/style/_vars.scss';

div{
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
</style>