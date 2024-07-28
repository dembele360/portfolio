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
          <v-tab>Projects</v-tab>
          <v-tab>Skills</v-tab>
          <v-tab>About</v-tab>
          <v-tab>Contacts</v-tab>
          <template>
            <v-btn icon @click="goToGitHub">
              <v-icon title="View on Github">mdi-github</v-icon>
            </v-btn>
          </template>
        </v-tabs>

      </div>
    </v-app-bar>

    <v-main>
      <MainScreen />
    </v-main>

    <v-footer class="d-flex flex-column" color="primary lighten-9" padless>
      <div class="bg-teal d-flex w-100 align-center px-4">
        <strong>Get connected with me on social networks!</strong>

        <v-spacer></v-spacer>

        <v-btn v-for="(icon, index) in icons" :key="index" icon @click="redirectToSocialMedia(icon)">
          <v-icon>{{ icon }}</v-icon>
        </v-btn>
      </div>

      <div class="px-4 py-2 bg-black text-center w-100">
        {{ new Date().getFullYear() }} — <strong>Musa Mustapha</strong>
      </div>
    </v-footer>
  </v-app>
</template>

<script>
import MainScreen from './components/MainScreen';


export default {
  name: 'App',

  components: {
    MainScreen,
  },

  data: () => ({
    icons: [
      'mdi-whatsapp',
      'mdi-facebook',
      'mdi-twitter',
      'mdi-linkedin',
      'mdi-instagram',
    ],
    methods: {
      goToGitHub() {
        window.open('https://github.com/dembele360/portfolio', '_blank');
      }
    },
  }),
};
</script>
