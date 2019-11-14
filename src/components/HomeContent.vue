<template>
  <v-container>
    <v-layout
      text-center
      wrap
    >
      <v-flex
        xs12
        mb-5
      >
        <h1 class="display-1 font-weight-bold mb-3">
          Willkommen auf der kleinen Code Demo :)
        </h1>
        <p class="subheading font-weight-bold mb-3">
          Folgende Dinge sind enthalten:
        </p>
        <v-layout justify-center>
          <v-chip outlined color="#60843e" ripple>Startseite</v-chip>
          <v-chip outlined color="#60843e" ripple>Star Wars Fakten - API Abfrage</v-chip>
          <v-chip outlined color="#60843e" ripple>Selbst geschossenen Fotos</v-chip>
          <v-chip outlined color="#60843e" ripple>Animationen aus Kundenprojekten</v-chip>
        </v-layout>
      </v-flex>

      <v-flex
        xs12
        mb-5
      >
        <p class="subheading font-weight-bold mb-3">
          Benutzte Technologien:
        </p>
        <v-layout justify-center>
          <v-timeline>
            <v-timeline-item color="#60843e"> HTML5</v-timeline-item>
            <v-timeline-item color="#8eaa3c" class="text-right"> CSS (SCSS)</v-timeline-item>
            <v-timeline-item color="#60843e">JS</v-timeline-item>
            <v-timeline-item color="#60843e">Vue.js</v-timeline-item>
            <v-timeline-item color="#8eaa3c">Vuetify</v-timeline-item>
            <v-timeline-item color="#60843e">GraphQL (Vue-Apollo.js)</v-timeline-item>
          </v-timeline>
        </v-layout>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: 'HomeContent',

  data: () => ({
    model: null,
  }),
};
</script>

<style lang="scss">
  .v-chip {
    margin: 8px;
  }
</style>
