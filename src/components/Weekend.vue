<template>
  <div class="WeekEnd-Component">
    <div class="weekend">
      <h2 v-if="weekend == false">
        {{ message }}
      </h2>
      <h2 v-else>It's weekend! :D</h2>
    </div>
    <div class="now">
      <h3>We are {{ day }}</h3>
      <h3>It's {{ time }}</h3>
    </div>
    <div class="gif">
      <div class="NotWe" v-if="gif == '0'">
        <img
          src="https://cdn.asthriona.com/i/2021/11/IMG_9556.jpg"
          height="300px"
          alt="Not We"
        />
      </div>
      <div class="we" v-if="gif == '1'">
        <img
          src="https://c.tenor.com/hSThcLBDUfwAAAAC/the-office-lets-party.gif"
          alt="We"
        />
      </div>
    </div>
  </div>
</template>

<script>
import dayjs from 'dayjs'
export default {
  name: 'App',
  data() {
    return {
      time: '',
      day: '',
      message: 'contacting the week end server... 彡ﾟ◉ω◉ )つー☆*',
      gif: '',
      weekend: false
    }
  },
  beforeMount () {
    this.time = dayjs().format('HH:mm:ss a')
    this.day = dayjs().format('dddd DD MMMM YYYY')
    setInterval(() => {
      this.time = dayjs().format('HH:mm:ss')
      this.day = dayjs().format('dddd DD MMMM YYYY')
      const weekDay = dayjs().format('dddd')
      const weekHours = dayjs().hour('HH')
      if (weekDay === 'Frieday' && weekHours >= '18') {
        this.weekend = true
        this.gif = '1'
      } else if (weekDay === 'Tuesday') {
        this.weekend = false
        this.gif = '0'
      } else if (weekDay === 'Frieday' && weekHours <= '18') {
        this.weekend = false
        this.message = 'Last Day!'
      } else {
        this.weekend = false
        this.message = "It's not weekend yet! :c"
      }
    }, 1000)
  }
}
</script>
