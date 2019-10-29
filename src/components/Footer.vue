<template>
  <v-card flat tile width="100%" class="grey lighten-4 text-center">
    <v-card-text>
      <v-btn class="mx-4" icon href="https://github.com/kevin-messiaen" target="_blank">
        <v-icon size="24px">mdi-github-circle</v-icon>
      </v-btn>
      <v-btn class="mx-4" icon href="https://www.linkedin.com/in/kevin-messiaen-074681188/" target="_blank">
        <v-icon size="24px">mdi-linkedin-box</v-icon>
      </v-btn>
    </v-card-text>

    <v-divider></v-divider>

    <v-card-text>
      &copy; {{ new Date().getFullYear() }} —
      <strong>Kevin Messiaen</strong>
    </v-card-text>
  </v-card>
</template>

<script>
export default {
  name: "Footer"
};
</script>

<style>
</style>