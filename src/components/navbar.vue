<template>
    <v-app-bar app prominent fixed dark class="site-header">
        <v-toolbar-title>
            <router-link to="/" tag="span" style="cursor: pointer">
                <img :src="appLogo" alt="Meraki Room Cicago" class="site-logo">
            </router-link>
        </v-toolbar-title>
        <v-spacer></v-spacer>
        <v-toolbar-items class="hidden-xs-only">
            <v-btn
            text
            v-for="item in menuItems"
            :key="item.title"
            :to="item.path">
            <v-icon left dark>{{ item.icon }}</v-icon>
            {{ item.title }}
            </v-btn>
        </v-toolbar-items>
    </v-app-bar>
</template>

<script>

export default {
  name: "navbar",
  data(){
    return {
      appTitle: 'Meraki Room Chicago',
      appLogo: 'MerakiRoomLogo.png',
      sidebar: false,
      menuItems: [
          { title: 'Home', path: '/', icon: 'mdi-home' },
          { title: 'Our Story', path: '/about', icon: 'mdi-face' },
          { title: 'Team', path: '/team', icon: 'mdi-lock_open' },
          { title: 'Services', path: '/services' },
          { title: 'Book Appointment', path: '/signin' },
     ]
    }
  },
};
</script>
<style>
.site-header {
    height: 3rem;
    overflow: auto;
}
.site-logo {
    width: 160px;
    position: relative;
    top: 8px;
}

</style>
