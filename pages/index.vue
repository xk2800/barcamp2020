<template>
  <body>
    <div id="social-icon" class="d-none d-md-block">
      <socialicon />
    </div>

    <div class="bg-barcamp">
      <div id="nav">
        <navbar />
      </div>

      <div id="home">
        <home />
      </div>
    </div>

    <b-container>
      <div id="about" class="pt-5 pb-5">
        <about />
      </div>
    </b-container>

    <!-- <div id="register" class="bg-barcamp">
      <register />
    </div> -->

    <div id="faq" class="pt-5 pb-5">
      <faq />
    </div>

    <div id="carousel">
      <carousel />
    </div>
  </body>
</template>

<script>
import Socialicon from '~/components/social-icons'
import Navbar from '~/components/navbar'
import Home from '~/components/home'
import About from '~/components/about'
import Carousel from '~/components/carousel'
import Faq from '~/components/faq'

export default {
  components: {
    Socialicon,
    Navbar,
    Home,
    About,
    Carousel,
    Faq
  }
}

window.onscroll = function () {
  scrollFunction()
}

function scrollFunction () {
  if (document.body.scrollTop > 20 || document.documentElement.scrollTop > 20) {
    document.getElementById('nav').style.top = '0'
  } else {
    document.getElementById('nav').style.top = '-70px'
  }
}
</script>

<style scoped>
  #nav {
  width: 100%;
  position: fixed;
  top: -70px;
  display: block;
  transition: top 0.3s;
  z-index: 9999;
}
</style>
