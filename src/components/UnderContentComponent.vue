<template>
  <section>
    <div class="container em-container">
      <ul>
        <li>
          <a href="#">
            <img src="../assets/img/buy-comics-digital-comics.png" alt="img">
            <span>digital comics</span>
          </a>
        </li>
        <li>
          <a href="#">
            <img src="../assets/img/buy-comics-merchandise.png" alt="img">
            <span>dc merchandise</span>
          </a>
        </li>
        <li>
          <a href="#">
            <img src="../assets/img/buy-comics-subscriptions.png" alt="img">
            <span>subscription</span>
          </a>
        </li>
        <li>
          <a href="#">
            <img src="../assets/img/buy-comics-shop-locator.png" alt="img">
            <span>comic shop locator</span>
          </a>
        </li>
        <li>
          <a href="#">
            <img src="../assets/img/buy-dc-power-visa.svg" alt="img">
            <span>dc power visa</span>
          </a>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: 'UnderContentComponent',
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
    li{
      z-index: 2;
      a{
        color: white;
        text-decoration: none;
        text-transform: uppercase;
        img{
          height: 55px;
          padding: 0 15px;
        }
        span{
          font-size: 14px;
          font-weight: 500;
        }
      }
    }
  }
  }
  
}
</style>