<template>
  <div class="timer">
    <span class="days">{{ days }}</span>Days
    <span class="hours">{{ hours }}</span>Hours
    <span class="minutes">{{ minutes }}</span>Minutes
    <span class="seconds">{{ seconds }}</span>Seconds
  </div>
</template>

<script>
  export default {
    data () {
      return {
        timer: undefined,
        days: 0,
        hours: 0,
        minutes: 0,
        seconds: 0
      }
    },

    methods: {
      prefixInteger (num, length) {
        return (Array(length).join('0') + num).slice(-length)
      },

      timeBetweenDates (loveDate) {
        const now = new Date()
        const difference = now.getTime() - loveDate.getTime()

        if (difference <= 0) {
          clearInterval(this.timer)
        } else {
          this.seconds = Math.floor(difference / 1000)
          this.minutes = Math.floor(this.seconds / 60)
          this.hours = Math.floor(this.minutes / 60)
          this.days = Math.floor(this.hours / 24)

          this.hours %= 24
          this.minutes %= 60
          this.seconds %= 60

          this.hours = this.prefixInteger(this.hours, 2)
          this.minutes = this.prefixInteger(this.minutes, 2)
          this.seconds = this.prefixInteger(this.seconds, 2)
        }
      }
    },

    mounted () {
      const that = this
      const loveDate = new Date('2017/08/13 23:30:00')
      this.timer = setInterval(() => {
        that.timeBetweenDates(loveDate)
      }, 1000)
    }
  }
</script>

<style scoped>
  .timer {
    position: absolute;
    bottom: 45rpx;
    width: 100%;
    text-align: center;
    color: #bd1521;
    font-size: 25rpx;
  }
  .days, .hours, .minutes, .seconds {
    font-size: 50rpx;
    color: #ffeb3b;
  }
</style>
