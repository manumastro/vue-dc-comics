<template>
  <nav>
          <ul>
            <li v-for="(el, index) in menuList" :key="`menu${index}`">
              <a
              :class="{ active : el.isActive }" 
              href="#">{{el.name}}</a>
            </li>

          </ul>
        </nav>
</template>

<script>
export default {
  name: 'NavComponent',
  props: {
    menuList: Array,
  }
}
</script>

<style lang="scss" scoped>
@import '../assets/style/_mixins.scss';
@import '../assets/style/_vars.scss';
nav{
      @include center;
      height: 100%;
      ul{
        display: flex;
        text-transform: uppercase;
        list-style: none;
        margin: auto;
        a{
          color: #464646;
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
            bottom: -53px;
            right: 0;
            width: 100%;
            border-bottom: 5px solid $primary-color;
          }
        }
        
      }
    }
</style>