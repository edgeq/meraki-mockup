<template>
    <v-app-bar app prominent dark class="site-header">
        <v-toolbar-title>
            <router-link to="/" tag="span" style="cursor: pointer">
                <img :src="appLogo" alt="Meraki Room Chicago" class="site-logo">
            </router-link>
        </v-toolbar-title>
        
        <v-spacer class="hidden-xs-only"></v-spacer>
        
        <v-toolbar-items class="hidden-xs-only">
            <v-btn
            text
            center
            v-for="item in menuItems"
            :key="item.title"
            :to="item.path">
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
    flex-shrink: 1;
}

@media screen and (max-width: 600px) {
    .v-toolbar--prominent .v-toolbar__content {
       justify-content: center
    }

    .site-logo {
        left: auto;
        top: 8px;
    }
}

@media only screen and (min-width: 600px) and (max-width: 768px) {
    .site-logo {
        display: none;
    }
}

</style>
