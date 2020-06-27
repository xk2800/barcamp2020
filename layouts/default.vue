<template>
  <div>
    <div>
      <nuxt />
    </div>
    <div id="footer">
      <Footer />
    </div>
  </div>
</template>

<script>
import Footer from '~/components/footer'

export default {
  components: {
    Footer
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Roboto:wght@100;300;400;500;700&display=swap');
  html {
    scroll-behavior: smooth;
  }

  body {
    font-family: 'Roboto', sans-serif;
  }

  .bg-none {
    background-color: #ffffff00;
  }

  .bg-pale {
    background-color: rgb(242, 243, 244);
  }

  .bg-nav {
    background-color:rgb(50,23,77);
  }

  .bg-barcamp {
    background-image: url('~assets/img/bg-barcamp.jpg');
    background-size: cover;
    background-attachment: fixed;
  }

  .text-purple {
    color:rgb(50,23,77);
  }

  .text-title {
    font-size:1.5em;
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
