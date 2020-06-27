<template>
  <div class="d-none d-sm-block mt-4 mb-4 animate__animated animate__fadeInUp animate__delay-1.2s">
    <b-row class="justify-content-md-center text-center text-white">
      <b-col col lg="1" class="roboto-thin days mr-2 p-2" style="font-size:4em">
        {{ displayDays }}
        <div class="absolute bottom-0 text-uppercase" style="font-size:0.25em">
          days
        </div>
      </b-col>
      <p class="roboto-thin p-1" style="font-size:4em">:</p>
      <b-col col lg="1" class="roboto-thin hours mr-2 p-2" style="font-size:4em">
        {{ displayHrs }}
        <div class="absolute bottom-0 text-uppercase" style="font-size:0.25em">
          hours
        </div>
      </b-col>
      <p class="roboto-thin p-1" style="font-size:4em">:</p>
      <b-col col lg="1" class="roboto-thin minutes mr-2 p-2" style="font-size:4em">
        {{ displayMins }}
        <div class="absolute bottom-0 text-uppercase" style="font-size:0.25em">
          minutes
        </div>
      </b-col>
      <p class="roboto-thin p-1" style="font-size:4em">:</p>
      <b-col col lg="1" class="roboto-thin seconds mr-2 p-2" style="font-size:4em">
        {{ displaySecs }}
        <div class="absolute bottom-0 text-uppercase" style="font-size:0.25em">
          seconds
        </div>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  data: () => ({
    displayDays: 0,
    displayHrs: 0,
    displayMins: 0,
    displaySecs: 0
  }),
  computed: {
    _seconds: () => 1000,
    _minutes () {
      return this._seconds * 60
    },
    _hours () {
      return this._minutes * 60
    },
    _days () {
      return this._hours * 24
    }
  },
  mounted () {
    this.showRemaining()
  },
  methods: {
    showRemaining () {
      const timer = setInterval(() => {
        const now = new Date()
        const deadline = new Date(2020, 7, 29, 10, 10, 10, 10)
        const diff = deadline.getTime() - now.getTime()

        if (diff < 0) {
          clearInterval(timer)
          return
        }

        const days = Math.floor((diff / this._days))
        const hours = Math.floor((diff % this._days) / this._hours)
        const minutes = Math.floor((diff % this._hours) / this._minutes)
        const seconds = Math.floor((diff % this._minutes) / this._seconds)

        this.displayDays = days < 10 ? '0' + days : days
        this.displayHrs = hours < 10 ? '0' + hours : hours
        this.displayMins = minutes < 10 ? '0' + minutes : minutes
        this.displaySecs = seconds < 10 ? '0' + seconds : seconds
      }, 1000)
    }
  }
}
</script>
