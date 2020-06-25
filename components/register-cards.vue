<template>
  <b-container class="pt-5 pb-5">
    <b-row class="justify-content-center">
      <b-col
        v-for="(card,i) in cards"
        :key="`card-${i}`"
        cols="10"
        lg="4"
        class="mt-2"
      >
        <b-card class="card-rounded bg-card">
          <b-card-text class="roboto-light text-center text-purple" style="font-size:1.5em;">
              {{ card.desc }}
          </b-card-text>
        </b-card>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
export default {
  data: () => {
    return {
      cards: [
        {
          desc: 'Register Here'
        },
        {
          desc: 'Sign Up as a Speaker'
        },
        {
          desc: 'Vote for Talks'
        }
      ]
    }
  }
}
</script>

<style scoped>
  .bg-card {
    background-color: rgba(255, 255, 255, 0.6);
  }

  .bg-card:hover {
    background-color: rgba(255, 255, 255, 0.5);
  }

  .card-rounded {
    border-radius: 2em 2em 2em 2em;
    box-shadow: 2px 2px 4px #000000;
  }
</style>
