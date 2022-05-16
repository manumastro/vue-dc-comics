<template>
  <section>
    <div class="container">
      <h3>Content goes here</h3>
    </div>
  </section>
</template>

<script>
export default {
  name: 'ContentComponent'
}
</script>

<style lang="scss" scoped>
@import '../assets/style/_mixins.scss';
  section{
    //padding: 50px 0;
    height: 140px;
    background-color: black;
    color: white;
    @include center-vertical;
  }
</style>