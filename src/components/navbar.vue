<template>
    <v-app-bar app prominent dark color="rgb(0,0,0,0.5)" class="site-header">
        <v-toolbar-title>
            <router-link to="/" tag="span" style="cursor: pointer">
                <img :src="appLogo" alt="Meraki Room Chicago" class="site-logo">
            </router-link>
        </v-toolbar-title>
        <v-spacer></v-spacer>
        <v-toolbar-items class="hidden-s-only">
            <v-btn
            text
            center
            v-for="item in menuItems"
            :key="item.title"
            :to="item.path">
            <!-- <v-icon left dark>{{ item.icon }}</v-icon> -->
            {{ item.title }}
            </v-btn>
        </v-toolbar-items>
    </v-app-bar>
</template>

<script>

export default {
  name: "Navbar",
  data(){
    return {
      appTitle: 'Meraki Room Chicago',
      appLogo: 'MerakiRoomLogo.png',
      menuItems: [
          { title: 'Home', path: '/' },
          { title: 'Our Story', path: '/about'},
          { title: 'Team', path: '/team' },
          { title: 'Services', path: '/services' },
          { title: 'Book Appointment', path: '/book' },
     ]
    }
  },
};
</script>
<style>
.v-toolbar__content {
  padding: 0 !important;
}

.site-logo {
    width: 160px;
    position: relative;
    top: 16px;
    left: 8px;
}

</style>
