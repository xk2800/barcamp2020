<template>
  <div>
    <b-carousel
      id="carousel-1"
      v-model="slide"
      :interval="3000"
      controls
      indicators
      img-width="1024"
      img-height="480"
      @sliding-start="onSlideStart"
      @sliding-end="onSlideEnd"
    >
      <!-- Slides with image only -->
      <b-carousel-slide img-src="~/assets/img/slider1.jpg" />
      <b-carousel-slide img-src="~/assets/img/slider2.jpg" />
      <b-carousel-slide img-src="~/assets/img/slider3.jpg" />
      <b-carousel-slide img-src="~/assets/img/slider4.jpg" />
    </b-carousel>
  </div>
</template>

<script>
export default {
  data () {
    return {
      slide: 0,
      sliding: null
    }
  },
  methods: {
    onSlideStart (slide) {
      this.sliding = true
    },
    onSlideEnd (slide) {
      this.sliding = false
    }
  }
}
</script>
