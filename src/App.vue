<template>
  <v-app>
    <Navbar />
    <v-app-bar-nav-icon class="mobile-menu d-flex d-sm-none" title="Menu" app @click.stop="drawer = !drawer">
      <v-icon class="mobile-menu-icon" right>{{mdiCaret}}</v-icon>
      <span class="mobile-menu-title">Menu</span>
    </v-app-bar-nav-icon>
    <v-navigation-drawer
      v-model="drawer"
      class="d-flex d-sm-none"
      app
      bottom
      temporary
    >
      <v-list
        nav
        dense
        v-for="item in mobileNav"
        :key="item.title"
      >
          <v-list-item>
            <v-list-item-title>
               <v-btn
                text
                center
                :to="item.path">
                  {{ item.title }}
                </v-btn>
            </v-list-item-title>
          </v-list-item>
          <v-divider></v-divider>
      </v-list>
    </v-navigation-drawer>

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
      drawer: false,
      group: null,
      mobileNav: [
        { title: 'Book Appointment', path: '/book' },
        { title: 'Our Story', path: '/about'},
        { title: 'Team', path: '/team' },
        { title: 'Services', path: '/services' },
        { title: 'Home', path: '/' },
          
      ]
    }
  },
  computed: {
    mdiCaret: function() {
      return this.drawer ? 'mdi-menu-down' : 'mdi-menu-right'
    }
  },
  watch: {
    group() {
      this.drawer = false
    },
  },
};
</script>

<style>
.mobile-menu {
  display: block;
  position: relative;
  top: 8rem;
}

.mobile-menu-title, .mobile-menu-icon {
  position: relative;
  left: 1rem;
}
</style>