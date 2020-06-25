<template>
  <b-navbar toggleable="lg" type="dark" class="fixed-top roboto-thin bg-nav">
    <b-navbar-brand href="#home">
      <b-img src="~/assets/img/barcamp-logo.png" style="height:2em" />
    </b-navbar-brand>

    <b-navbar-toggle target="nav-collapse" />

    <b-collapse id="nav-collapse" is-nav>
      <!-- Right aligned nav items -->
      <b-navbar-nav class="ml-auto text-white">
        <b-nav-item
          v-for="(item,i) in homeitems"
          :key="`item-${i}`"
          :href="`#${item.destination}`"
          class="nav-item"
        >
          {{ item.navitem }}
        </b-nav-item>
        <b-nav-item
          v-for="(item,i) in externalitems"
          :key="`item-${i}`"
          :href="`${item.destination}`"
          target="_blank"
          class="nav-item"
        >
          {{ item.navitem }}
        </b-nav-item>
      </b-navbar-nav>
    </b-collapse>
  </b-navbar>
</template>

<script>
export default {
  data: () => {
    return {
      homeitems: [
        {
          navitem: 'Home',
          destination: 'home'
        },
        {
          navitem: 'About',
          destination: 'about'
        },
        {
          navitem: 'FAQ',
          destination: 'faq'
        },
        {
          navitem: 'Sponsors',
          destination: 'sponsor'
        },
        {
          navitem: 'Agenda',
          destination: 'agenda'
        }
      ],
      externalitems: [
        {
          navitem: 'Vote for Talks',
          destination: 'https://polys.me/'
        }
      ]
    }
  }
}
</script>

<style scoped>
  .nav-item {
    padding-left: 0.5em;
    padding-right: 0.5em;
    font-size: 1.2em;
  }
</style>
