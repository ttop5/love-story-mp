<template>
  <div>
    <h1 class="title">LOVE STORY</h1>
    <timer></timer>
  </div>
</template>

<script>
  import timer from '@/components/timer'

  export default {
    components: {
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
  .title {
    text-align: center;
    font-size: 45rpx;
  }
</style>
