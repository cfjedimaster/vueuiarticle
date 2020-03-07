<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >

      <!-- this was an option I considered...
      <v-btn icon to="/">
        <v-icon>mdi-home</v-icon>
      </v-btn>
      -->
      <v-toolbar-title>UI Demo</v-toolbar-title>

      <template v-slot:extension>
        <v-tabs align-with-title>
          <v-tab to="/">Home</v-tab>
          <v-tab to="/cats">Cats</v-tab>
          <v-tab to="/pics">Pictures</v-tab>
          <v-tab to="/contact">Contact</v-tab>
        </v-tabs>
      </template>
    </v-app-bar>

    <v-content class="ma-5">
      <router-view/>
    </v-content>
  </v-app>
</template>

<script>

export default {
  name: 'App',
  data: () => ({
    //
  }),
};
</script>
