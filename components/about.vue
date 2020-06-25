<template>
  <div>
    <h3 class="animate__animated animate__fadeInLeft animate__delay-1.4s">
      <b class="roboto-fat text-purple" style="font-size:1.5em; letter-spacing:2px;">BarCamp</b>
    </h3>
    <h5 class="roboto-light animate__animated animate__fadeInLeft animate__delay-1.5s text-purple" style="line-height:1.5em;">
      {{ aboutDesc }}
    </h5>
  </div>
</template>

<script>
export default {
  data: () => {
    return {
      aboutDesc: 'is a user-generated conference that brings people together to share their passion. There is no preset of speakers for BarCamp like usual conferences.'
    }
  }
}
</script>
