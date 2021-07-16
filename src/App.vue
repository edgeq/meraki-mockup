<template>
  <v-app>
    <navbar />
    
    <v-content>
      <router-view />
    </v-content>

    <footernav />
  </v-app>
</template>

<script>
import navbar from './components/navbar';
import footernav from './components/footernav';

export default {
  name: 'App',

  components: {
    navbar,
    footernav,
  },

  data() {
    return {
      appName: "Mearki Room Chicago"
    }
  },
};
</script>
