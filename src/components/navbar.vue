<template>
  <div class="site-nav">
    <v-app-bar app prominent dark class="site-header">
      <v-toolbar-title>
        <router-link to="/" tag="span" style="cursor: pointer">
          <img :src="appLogo" alt="Meraki Room Chicago" class="site-logo" />
        </router-link>
      </v-toolbar-title>

      <v-spacer></v-spacer>

      <v-app-bar-nav-icon
        app
        class="mobile-menu-icon d-flex d-sm-none"
        x-large
        @click.stop="drawer = !drawer"
      >
        <v-icon class="mobile-menu-icon">mdi-menu</v-icon>
      </v-app-bar-nav-icon>

      <v-toolbar-items class="hidden-xs-only">
        <v-btn
          text
          center
          v-for="item in menuItems"
          :key="item.title"
          :to="item.path"
        >
          {{ item.title }}
        </v-btn>
      </v-toolbar-items>
    </v-app-bar>

    <v-navigation-drawer
      v-model="drawer"
      class="d-flex d-sm-none"
      app
      bottom
      temporary
    >
      <v-list nav dense v-for="item in mobileNav" :key="item.title">
        <v-list-item>
          <v-list-item-title>
            <v-btn text block :to="item.path">
              {{ item.title }}
            </v-btn>
          </v-list-item-title>
        </v-list-item>
        <v-divider></v-divider>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>

<script>
export default {
  name: "Navbar",
  data() {
    return {
      appTitle: "Meraki Room Chicago",
      appLogo: "MerakiRoomLogo.png",
      menuItems: [
        { title: "Home", path: "/" },
        { title: "Our Story", path: "/about" },
        { title: "Team", path: "/team" },
        { title: "Services", path: "/services" },
        { title: "Book Appointment", path: "/book" },
      ],
      drawer: false,
      group: null,
      mobileNav: [
        { title: "Home", path: "/" },
        { title: "Book Appointment", path: "/book" },
        { title: "Services", path: "/services" },
        { title: "Our Story", path: "/about" },
        { title: "Team", path: "/team" },
      ],
    };
  },
  watch: {
    group() {
      this.drawer = false;
    },
  },
};
</script>
<style>
.v-toolbar__content {
  padding: 0 !important;
}

.site-header {
  padding: 0 1rem;
}

.site-logo {
  width: 160px;
  position: relative;
  top: 12px;
  flex-shrink: 1;
}

.mobile-menu-icon {
  align-self: center;
}
</style>
