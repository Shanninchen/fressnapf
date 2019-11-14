<template>
  <v-bottom-navigation
    v-model="bottomNav"
    color="#fff"
    grow
    fixed
    app
    dark
  >
    <v-btn value="home" to="/">
      <span>Home</span>
      <v-icon>mdi-home</v-icon>
    </v-btn>

    <v-btn value="starwars" to="/starwars">
      <span>Star Wars</span>
      <v-icon>mdi-death-star</v-icon>
    </v-btn>

    <v-btn value="images" to="/images">
      <span>Images</span>
      <v-icon>mdi-image</v-icon>
    </v-btn>

    <v-btn value="animations" to="/animations">
      <span>Animations</span>
      <v-icon>mdi-auto-fix</v-icon>
    </v-btn>
  </v-bottom-navigation>
</template>

<script>
export default {
  name: 'BottomNavigation',
  data() {
    return {
      bottomNav: 'home',
    };
  },
};
</script>

<style lang="scss">
  .v-btn:not(.v-btn--round).v-size--default {
    height: auto !important;
  }
</style>
