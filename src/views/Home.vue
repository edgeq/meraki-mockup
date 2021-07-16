<template>
  <div class="home">
    <v-card 
      class="home-card pa-16 mb-8"
      dark
      elevation="4"
      outlined
      shaped
      >
      <h1 class="display-1">A full service salon in the heart of wicker park</h1>
    </v-card>
    <v-btn 
    elevation="2"
    rounded
    color="white"
    class="pa-8"
    x-large><span class="display-1">Book An Appointment</span></v-btn>
  </div>
</template>

<script>
  export default {
    name: 'Home',
    data() {
      return {
        'homeImg': '/img/ig_meraki_03.jpeg'
      }
    },
    computed: {
      innerHeight() {
        return window.innerHeight;
      }
    }
  }
</script>

<style>
.home {
  background-image: url('/img/ig_meraki_03.jpeg');
  background-size: cover;
  background-position: bottom;
  height: 100vh;

  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>
