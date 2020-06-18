<template>
  <body>
    <div class="bg-barcamp">
      <div id="nav_bar">
        <b-navbar toggleable="lg" type="dark" class="roboto-thin bg-nav">
          <b-navbar-brand href="#">
            NavBar
          </b-navbar-brand>

          <b-navbar-toggle target="nav-collapse" />

          <b-collapse id="nav-collapse" is-nav>
            <!-- Right aligned nav items -->
            <b-navbar-nav class="ml-auto text-white">
              <b-nav-item href="#" class="nav-item">
                Home
              </b-nav-item>
              <b-nav-item href="#" class="nav-item">
                About
              </b-nav-item>
              <b-nav-item href="#" disabled class="nav-item">
                Vote for Talks
              </b-nav-item>
              <b-nav-item href="#" class="nav-item">
                FAQ
              </b-nav-item>
              <b-nav-item href="#" disabled class="nav-item">
                Agenda
              </b-nav-item>
              <b-nav-item href="#" class="nav-item">
                Sponsors
              </b-nav-item>
            </b-navbar-nav>
          </b-collapse>
        </b-navbar>
      </div>

      <div id="home">
        <b-container fluid class="p-4">
          <b-row>
            <b-col cols="12">
              <b-card class="bg-none text-center border-0 animate__animated animate__fadeInUp">
                <b-img src="~/assets/img/barcamp-logo.png" fluid />
              </b-card>
              <b-card class="bg-none text-center text-white Roboto-light border-0 animate__animated animate__fadeInUp animate__delay-1.2s">
                <p class="d-none d-lg-block roboto-light" style="font-size:3em">
                  9am to 6pm on <b class="roboto-fat" style="font-size:1.5em">August 29</b> 2020
                </p>
                <p class="d-lg-none d-sm-block roboto-light" style="font-size:1.2em">
                  9am to 6pm on <b class="roboto-fat" style="font-size:1.5em">August 29</b> 2020
                </p>
              </b-card>
            </b-col>
          </b-row>
          <b-row class="pt-4 pb-5 text-center animate__animated animate__fadeInUp animate__delay-1.3s">
            <b-col>
              <b-button variant="outline-light" size="lg" class="p-3 mr-1" style="width:8.5em" pill>
                Be a Speaker
              </b-button>
              <b-button variant="light" size="lg" class="p-3 ml-1" style="width:8.5em; color:purple;" pill>
                Register Now
              </b-button>
            </b-col>
          </b-row>
        </b-container>
      </div>
    </div>
    <b-container>
      <div id="about" class="pt-5 pb-5">
        <h1 class="animate__animated animate__fadeInLeft animate__delay-1.4s">
          <b class="roboto-fat text-purple" style="font-size:1.5em; letter-spacing:2px;">BarCamp</b>
        </h1>
        <h4 class="roboto-light animate__animated animate__fadeInLeft animate__delay-1.5s text-purple" style="line-height:1.5em;">
          is a user-generated conference that brings people together to share their passion. There is no preset of speakers for BarCamp like usual conferences.
        </h4>
      </div>
    </b-container>
    <div id="register" class="bg-barcamp">
      <b-container class="pt-5 pb-5">
        <b-row>
          <b-col cols="12" lg="4" class="mt-2">
            <b-card class="card-rounded bg-card">
              <b-card-text class="roboto-light text-center text-purple" style="font-size:2em">
                Register Here
              </b-card-text>
            </b-card>
          </b-col>
          <b-col cols="12" lg="4" class="mt-2">
            <b-card class="card-rounded bg-card">
              <b-card-text class="roboto-light text-center text-purple" style="font-size:2em">
                Sign Up as a Speaker
              </b-card-text>
            </b-card>
          </b-col>
          <b-col cols="12" lg="4" class="mt-2">
            <b-card class="card-rounded bg-card">
              <b-card-text class="roboto-light text-center text-purple" style="font-size:2em">
                Vote for Talks
              </b-card-text>
            </b-card>
          </b-col>
        </b-row>
      </b-container>
    </div>
    <div id="carousel">
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
    </div>
  </body>
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
  },
  head: {
    link: [
      { rel: 'stylesheet', href: 'https://cdnjs.cloudflare.com/ajax/libs/animate.css/4.0.0/animate.min.css' }
    ]
  }
}
</script>

<style scoped>
  @import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;400;500;700&display=swap');

  body {
    font-family: 'Roboto', sans-serif;
  }

  .nav-item {
    padding-left: 0.5em;
    padding-right: 0.5em;
    font-size: 1.2em;
  }

  .bg-none {
    background-color: #ffffff00;
  }

  .bg-nav {
    background-color: rgba(112,128,144,0.8);
  }

  .bg-card {
    background-color: rgba(255, 255, 255, 0.6);
  }

  .bg-card:hover {
    background-color: rgba(255, 255, 255, 0.5);
  }

  .bg-barcamp {
    background-image: url('~assets/img/bg-barcamp.jpg');
    background-size: cover;
    background-attachment: fixed;
  }

  .text-purple {
    color:rgb(50,23,77);
  }

  .card-rounded {
    border-radius: 2em 2em 2em 2em;
    box-shadow: 2px 2px 4px #000000;
  }

  .roboto-thin {
    font-family: 'Roboto', sans-serif;
    font-weight: 100;
  }

  .roboto-light {
    font-family: 'Roboto', sans-serif;
    font-weight: 300;
  }

  .roboto-medium {
    font-family: 'Roboto', sans-serif;
    font-weight: 400;
  }

  .roboto-fat {
    font-family: 'Roboto', sans-serif;
    font-weight: 500;
  }
</style>
