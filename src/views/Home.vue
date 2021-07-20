<template>
  <div class="home">
    
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
  height: 75vh; /* placeholder until there's stuff to fill the gap. */
  width: 100%;
  overflow: auto;
  
}

.home-content {
  flex-direction: column;
  display: flex;
  align-items: flex-start;
  justify-content: center;
  position: relative;
  overflow:visible;
}


</style>
