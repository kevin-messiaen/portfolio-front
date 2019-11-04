<template>
  <v-footer app absolute class="font-weight-medium" dark>
    <v-col class="text-center" cols="12">
      {{ new Date().getFullYear() }} &copy;
      <strong>Kevin Messiaen</strong>
    </v-col>
    <v-btn
      fab
      large
      absolute
      right
      top
      color="primary"
      dark
      @click="$vuetify.goTo(top, options)"
    >
      <v-icon>mdi-chevron-up</v-icon>
    </v-btn>
  </v-footer>
</template>

<script>
export default {
  data() {
    return {
      top: 0,
      options: {
        duration: 300,
        offset: 0,
        easing: "easeInOutCubic"
      }
    };
  }
};
</script>

<style>
</style>