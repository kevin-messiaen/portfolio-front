<template>
  <v-app>
    <v-app-bar app>
      <v-toolbar-title class="headline text-uppercase">
        <span>Kevin</span>
        <span class="font-weight-light"> MESSIAEN</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        text
        href="https://github.com/vuetifyjs/vuetify/releases/latest"
        target="_blank"
      >
        <span class="mr-2">Latest Release</span>
        <v-icon>mdi-open-in-new</v-icon>
      </v-btn>
    </v-app-bar>

    <v-content>
      <Home/>
    </v-content>

    <v-footer padless="true">
      <Footer/>
    </v-footer>
  </v-app>
</template>

<script>
import Home from './components/Home';
import Footer from './components/Footer'

export default {
  name: 'App',
  components: {
    Home,
    Footer
  },
  data: () => ({
    //
  }),
};
</script>
