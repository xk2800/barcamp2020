<template>
  <b-container fluid class="p-4">
    <b-row class="pt-5">
      <b-col cols="12">
        <b-card class="bg-none text-center border-0 animate__animated animate__fadeInUp">
          <b-img src="~/assets/img/barcamp-logo.png" fluid />
        </b-card>
        <b-card class="bg-none text-center text-white Roboto-light border-0 animate__animated animate__fadeInUp animate__delay-1.2s">
          <p class="d-none d-lg-block roboto-light" style="font-size:3em">
            <b class="roboto-fat" style="font-size:1.5em">{{ date }}</b> 2020
          </p>
          <p class="d-none d-lg-block roboto-light" style="font-size:3em">
            {{ time }}
          </p>
          <p class="d-lg-none d-sm-block roboto-light" style="font-size:1.2em">
            <b class="roboto-fat" style="font-size:1.5em">{{ date }}</b> 2020
          </p>
          <p class="d-lg-none d-sm-block roboto-light" style="font-size:1.2em">
            {{ time }}
          </p>
        </b-card>
      </b-col>
    </b-row>
    <b-row class="pt-4 pb-5 text-center animate__animated animate__fadeInUp animate__delay-1.3s">
      <b-col>
        <b-button variant="outline-light" size="md" class="p-3 mr-1" style="width:8.5em" pill>
          Be a Speaker
        </b-button>
        <b-button variant="light" size="md" class="p-3 ml-1" style="width:8.5em; color:purple;" pill>
          Register Now
        </b-button>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  data: () => {
    return {
      date: 'August 29',
      time: '1.30 to 7.20pm'
    }
  }
}
</script>
