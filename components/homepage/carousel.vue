<template>
  <div class="carousel">
    <v-carousel
      :show-arrows="true"
      :cycle="true"
    >
      <v-carousel-item
        v-for="(color, index) in colors"
        :key="index"
      >
        <p>nigga</p>
      </v-carousel-item>
    </v-carousel>
  </div>
</template>

<script>
export default {
  data () {
    return {
      colors: ['red', 'green', 'purple']
    }
  }
}
</script>

<style>

</style>
