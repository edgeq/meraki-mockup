<template>
  <div class="home">
    <div class="home-content pa-4">
      <div class="heading pa-2">
        <h1 class="heading-title white--text">MERAKI ROOM CHICAGO</h1>
        <h2 class="heading-sub white--text">A full service salon in the heart of Wicker Park.</h2>
      </div>
      <v-btn class="mt-3" to="/book">Book an Appointment</v-btn>
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
  height: 60vh;
  width: 100%;
  overflow: auto;
  
}

.home-content {
  height: 100%;
  flex-direction: column;
  display: flex;
  position: relative;
  overflow:visible;
}

.heading {
  background-color: rgba(0,0,0,0.8);
  border-radius: 4px;
}

.heading-title, .heading-sub {
  font-weight: 100;
}

@media screen and (min-width: 600px) {
  .home-content {
    align-items: flex-start;
    justify-content: center;

  }
}


</style>
