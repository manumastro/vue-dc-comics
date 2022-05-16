<template>
  <footer>
    <section class="info-section">
      <div class="container em-container">
        <div class="info">
          <ul>
          <li class="type mb-2 ">DC COMICS</li>
          <li><a href="#">Characters</a></li>
          <li><a href="#">Comics</a></li>
          <li><a href="#">Movies</a></li>
          <li><a href="#">TV</a></li>
          <li><a href="#">Games</a></li>
          <li><a href="#">Videos</a></li>
          <li class="mb-3"><a href="#">News</a></li>
          <li class="type mb-2">SHOP</li>
          <li><a href="#">Shop DC</a></li>
          <li><a href="#">Shop DC Collectibles</a></li>
        </ul>
        <ul>
          <li class="type mb-2 ">DC</li>
          <li><a href="#">Terms Of Use</a></li>
          <li><a href="#">Privacy policy (New)</a></li>
          <li><a href="#">Ad Choices</a></li>
          <li><a href="#">Advertising</a></li>
          <li><a href="#">Jobs</a></li>
          <li><a href="#">Subscription</a></li>
          <li><a href="#">Talent Workshops</a></li>
          <li><a href="#">CPSC Certificates</a></li>
          <li><a href="#">Ratings</a></li>
          <li><a href="#">Shop Help</a></li>
          <li><a href="#">Contact Us</a></li>
        </ul>
        <ul>
          <li class="type mb-2 ">SITES</li>
          <li><a href="#">DC</a></li>
          <li><a href="#">MAD Magazine</a></li>
          <li><a href="#">DC Universe</a></li>
          <li><a href="#">DC Power Visa</a></li>
        </ul>
        </div>
        <div class="logo-bg">
          <img src="../assets/img/dc-logo-bg.png" alt="">
        </div>
      </div>
    </section>

    <section class="signup-social">
      <div class="container d-flex justify-content-between ">
        <div class="signup">
          <button>SIGN-UP NOW!</button>
        </div>
        <div class="social d-flex align-items-center">
          <span>FOLLOW US</span>
          <a href="#"><img src="../assets/img/footer-facebook.png" alt="facebook"></a>
          <a href="#"><img src="../assets/img/footer-periscope.png" alt="periscope"></a>
          <a href="#"><img src="../assets/img/footer-pinterest.png" alt="pinterest"></a>
          <a href="#"><img src="../assets/img/footer-twitter.png" alt="twitter"></a>
          <a href="#"><img src="../assets/img/footer-youtube.png" alt="youtube"></a>
        </div>
      </div>
    </section>
  </footer>
</template>

<script>
export default {
  name: 'FooterComponent'
}
</script>

<style lang="scss" scoped>
@import '../assets/style/_vars.scss';
@import '../assets/style/_mixins.scss';
  footer{
    //min-height: calc(100% - 420px);
    .info-section{
      background-image: url('../assets/img/footer-bg.jpg');
      background-size: cover;
      background-position: center;
      .em-container{
        display: flex;
        &>div{
          width: 50%;
        }
      }
      .info{
        display: flex;
        ul{
          padding: 40px 50px 50px 0;
        }
        li{
          list-style: none;
          line-height: 22px;
          &.type{
            color: white;
            font-size: 20px;
          }
          a{
            color: grey;
            font-size: 13px;
            font-weight: 500;
            text-decoration: none;
            transition: color 0.1s;
            &:hover{
              color: $primary-color;
            }
          }
        }
      }
      .logo-bg{
        position: relative;
        img{
          position: absolute;
          top: -97px;
          right: 0;
          z-index: 1;
        }
      }
    }
    .signup-social{
      @include center;
      min-height: 136px;
      position: relative;
      background-color: #303030;
      z-index: 3;
      .signup{
        button{
        color: whitesmoke;
        font-weight: 500;
        font-size: 18px;
        background-color: #303030;
        padding: 10px;
        border-color: $primary-color;
        transition: background-color 0.3s ease-in-out;
        &:hover{
          background-color: $primary-color;
        }
      }
      }
      .social{
        span{
          color: $primary-color;
          font-weight: 600;
          font-size: 20px;
        }
        span, a{
          margin-right: 20px;
        }
      }

    }
    
  }
</style>