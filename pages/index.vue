<template>
  <body>
    <div class="bg-barcamp">
      <div id="nav_bar">
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

    <div id="register" class="bg-barcamp">
      <register />
    </div>

    <div id="carousel">
      <carousel />
    </div>

    <div id="faq" class="pt-5 pb-5">
      <faq />
    </div>
  </body>
</template>

<script>
import Navbar from '~/components/navbar'
import Home from '~/components/home'
import About from '~/components/about'
import Register from '~/components/register-cards'
import Carousel from '~/components/carousel'
import Faq from '~/components/faq'

export default {
  components: {
    Navbar,
    Home,
    About,
    Register,
    Carousel,
    Faq
  }
}
</script>
