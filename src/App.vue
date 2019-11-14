<template>
  <v-app>
    <v-app-bar
      app
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Fressnapf Logo"
          class="shrink mr-2"
          contain
          src="./assets/logo.svg"
          transition="scale-transition"
          width="50"
        />
      </div>
    </v-app-bar>
    <v-content>
      <router-view></router-view>
    </v-content>
    <v-footer app>
      <v-spacer></v-spacer>
      <div>&copy; {{ new Date().getFullYear() }}</div>
    </v-footer>
    <BottomNavigation></BottomNavigation>
  </v-app>
</template>

<script>
import BottomNavigation from './components/navigation/BottomNavigation.vue';

export default {
  name: 'App',

  components: {
    BottomNavigation,
  },
};
</script>

<style lang="scss">
  body {
    background-color: #eeedeb;
    color: #333 !important;
  }

  header.v-toolbar,
 .v-bottom-navigation {
    background: linear-gradient(to bottom,#8eaa3c 0,#60843e 100%);
  }

  h1 {
    color: #60843e;
    text-shadow: 0 2px 2px rgba(12,24,27,.2);
  }
</style>
