<template>
  <div class="container">
    <div class="heart">
      <div class="beat">
        <a href="#" target="_blank">
          <div class="left"></div>
          <div class="right"></div>
          <div class="bottom"></div>
        </a>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
  }
</script>

<style scoped>
  @keyframes float {
    from {
      transform: translateY(0px);
    }
    to {
      transform: translateY(-15px);
    }
  }
  @keyframes shadow {
    to {
      transform: scale(1.2);
    }
  }
  @keyframes heartbeat {
    0% {
      transform: scale(1);
    }
    40% {
      transform: scale(1);
    }
    44% {
      transform: scale(1.03);
    }
    50% {
      transform: scale(1);
    }
    52% {
      transform: scale(1.04);
    }
    58% {
      transform: scale(1);
    }
  }
  .heart {
    animation: float 0.8s cubic-bezier(0, 0.5, 0.5, 1) infinite alternate;
    position: absolute;
    z-index: -10;
  }
  .heart div.beat {
    animation: heartbeat 1.6s infinite;
    content: '';
    display: block;
  }
  .heart .left {
    height: 100px;
    width: 100px;
    background: #bd1521;
    border-radius: 100%;
    content: '';
    display: block;
  }
  .heart .right {
    height: 100px;
    width: 100px;
    background: #bd1521;
    border-radius: 100%;
    content: '';
    display: block;
    transform: translate(70px, -100px);
  }
  .heart .bottom {
    height: 100px;
    width: 100px;
    background: #bd1521;
    border-bottom-right-radius: 10px;
    content: '';
    display: block;
    transform: rotate(45deg) translate(-92px, -141px);
  }
  .shadow {
    animation: shadow 0.8s cubic-bezier(0, 0.5, 0.5, 1) infinite alternate;
    background: #c7c7c7;
    border-radius: 100%;
    content: '';
    display: block;
    position: absolute;
    top: 175px;
    left: 60px;
    height: 12px;
    width: 50px;
  }
  .container {
    transform: translate(-70rpx, 50%);
  }
  p {
    color: #323232;
    font-family: 'Open Sans';
    font-size: 12px;
    left: 20px;
    position: relative;
    text-decoration: none;
    top: 200px;
  }
  p:hover {
    color: #c7c7c7;
  }
</style>
