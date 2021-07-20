<template>
  <div class="home">
    <div class="home-content pa-4">
      <h1 class="white--text">Meraki Room Chicago</h1>
      <h3 class="white--text">A full service salon in the heart of Wicker Park.</h3>
      <v-btn class="mt-3">Book an Appointment</v-btn>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Home',
    data() {
      return {}
    }
  }
</script>

<style>
.home {
  background-image: url('/img/ig_meraki_03.jpeg');
  background-position: 75% 80%;
  background-size: cover;
  height: 66vh;
  width: 100%;
  overflow: auto;
  
}

.home-content {
  background-color: rgba(0,0,0,0.5);
  height: 100%;
  flex-direction: column;
  display: flex;
  align-items: flex-start;
  justify-content: center;
  position: relative;
  overflow:visible;
}


</style>
