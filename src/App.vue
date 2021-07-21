<template>
  <v-app class="pa-0 ma-0">
    <Navbar />

      <v-main>
        <router-view />
      </v-main>

    <Footer />
  </v-app>
</template>

<script>
import Navbar from './components/Navbar';
import Footer from './components/Footer';

export default {
  name: 'App',

  components: {
    Navbar,
    Footer,
  },

  data() {
    return {
      appName: "Meraki Room Chicago",
    }
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@300;400;600;700&family=Josefin+Slab:ital,wght@0,100;1,100&display=swap');

.v-application {
  font-family: 'Josefin Sans', sans-serif;;
}

</style>