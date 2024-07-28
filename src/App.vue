<template>
  <v-app>
    <v-app-bar app color="#1a180e" dark :style="{ height: '10%', margin: '0 auto' }">
      <div class="d-flex align-center">
        <v-img alt="Vuetify Logo" class="shrink mr-2" contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png" transition="scale-transition" width="40" />
        <v-toolbar-title>Mussa's Professional Portfolio</v-toolbar-title>
      </div>

      <v-spacer></v-spacer>

      <div class="d-flex align-right">
        <v-tabs align-with-title background-color="#1a180e" dark>
          <v-tab>Home</v-tab>
          <v-tab>Experience</v-tab>
          <v-tab>Contacts</v-tab>
        </v-tabs>
      </div>
    </v-app-bar>

    <v-main>
      <HelloWorld />
    </v-main>

    <v-footer color="primary lighten-9" padless>
      <v-row justify="center" no-gutters>
        <v-btn v-for="link in links" :key="link" color="white" text rounded class="my-2">
          {{ link }}
        </v-btn>
        <v-col class="primary lighten-2 py-4 text-center white--text" cols="12">
          {{ new Date().getFullYear() }} — <strong>Developed by Mussa</strong>
        </v-col>
      </v-row>
    </v-footer>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    //
  }),
};
</script>
