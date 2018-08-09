<template>
  <div class="home">
    <!--<h1 class="title">LOVE STORY</h1>-->
    <h5>❤️-hyh 2017-08-13 tlx-❤️</h5>
    <main class="scene">
      <heart></heart>
      <timer></timer>
    </main>
  </div>
</template>

<script>
  import heart from '@/components/heart'
  import timer from '@/components/timer'

  export default {
    components: {
      heart,
      timer
    },

    data () {
      return {
      }
    },

    methods: {}
  }
</script>

<style scoped>
  .home {
  }
  .title {
    font-size: 45rpx;
  }
  h5 {
    text-align: center;
  }
</style>
