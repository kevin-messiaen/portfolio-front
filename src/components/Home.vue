<template>
  <v-container>
    <p class="text-justify headline">Je suis un développeur fullstack spécialisé dans la téchnique.</p>
    <v-row
      justify="center"
      class="d-none d-sm-flex">
      <v-col
        cols="9"
        class="d-none d-sm-flex d-md-none">
        <Contact />
      </v-col>
      <v-col
        cols="6"
        class="d-none d-md-flex">
        <Contact />
      </v-col>
    </v-row>
    <Contact class="d-flex d-sm-none"/>
  </v-container>
</template>

<script>
import Contact from "./Contact";

export default {
  name: "Home",
  components: {
    Contact
  }
};
</script>