<template>
  <div>
    <b-row>
      <b-col col="12" lg="7">
        <h3 class="animate__animated animate__fadeInLeft animate__delay-1.4s">
          <b class="roboto-fat text-purple text-title">BarCamp Cyberjaya</b>
        </h3>
        <h4 class="animate__animated animate__fadeInLeft animate__delay-1.4s">
          <b class="roboto-fat text-purple">Share | Learn | Inspire</b>
        </h4>
        <h5 class="roboto-light animate__animated animate__fadeInLeft animate__delay-1.5s text-purple text-justify mt-3" style="line-height:1.5em;">
          {{ aboutDesc }}
        </h5>
        <b-row class="mt-4 d-none d-sm-block">
          <b-col>
            <b-button variant="outline-light" size="lg" class="abt-btn p-3 mr-1" pill>
              Be a Speaker
            </b-button>
            <b-button variant="outline-light" size="lg" class="abt-btn p-3 ml-1" pill>
              Be a Sponsor
            </b-button>
          </b-col>
        </b-row>
        <b-row class="mt-4 d-block d-sm-none">
          <b-col>
            <b-button variant="outline-light" size="md" class="abt-btn p-3 mr-1" pill>
              Be a Speaker
            </b-button>
            <b-button variant="outline-light" size="md" class="abt-btn p-3 ml-1" pill>
              Be a Sponsor
            </b-button>
          </b-col>
        </b-row>
      </b-col>
    </b-row>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      aboutDesc: 'Barcamp Cyberjaya is an international network of user-generated conference that brings people together to share their passion around technology. There is no preset of speakers for BarCamp like usual conferences. Participants get to vote for speakers based on the topics proposed by speakers.'
    }
  }
}
</script>

<style scoped>
  .abt-btn {
    width:8.5em;
    color:white;
    border-color:rgb(108,48,130);
    background-color: rgb(108,48,130);
  }

  .abt-btn:hover {
    width:8.5em;
    color:rgb(108,48,130);
    border-color:rgb(108,48,130);
    background-color: white;
  }
</style>
