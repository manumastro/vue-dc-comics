<template>
  <div>
    <li>
      <a href="#">
        <img :src="card.image" :alt="card.name">
        <span>{{card.name}}</span>
      </a>
    </li>
  </div>
</template>

<script>
export default {
  name: 'UnderContentCards',
  props: {
    card: Object,
  }
}
</script>

<style lang="scss" scoped>
li{
      position: relative;
      z-index: 3;
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
</style>