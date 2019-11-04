<template>
  <div id="about" class="container">
    <v-row justify="center" class="pt-12">
      <v-col cols="12" md="6" class="text-center">
        <v-avatar size="256">
          <img src="../assets/profile_picture.jpeg" alt="Kevin Messiaen" />
        </v-avatar>
      </v-col>
      <v-col cols="12" md="6" class="px-8">
        <p class="display-3">À propos</p>
        <p class="headline text-justify">Jeune diplômé de master MIAGE</p>
        <p
          class="body-1 text-justify"
        >Je mets mes compétences de développeur à profit de vos projets afin de créer des sites web et applications sur mesure.</p>
      </v-col>
    </v-row>
    <v-row justify="center" align="center">
      <v-col cols="12" md="6" class="px-8">
        <v-row align="center">
          <v-col cols="4" class="text-right">Spring Boot</v-col>
          <v-col cols="8">
            <v-progress-linear value="90"></v-progress-linear>
          </v-col>
        </v-row>
        <v-row align="center">
          <v-col cols="4" class="text-right">Vue.js</v-col>
          <v-col cols="8">
            <v-progress-linear value="80"></v-progress-linear>
          </v-col>
        </v-row>
        <v-row align="center">
          <v-col cols="4" class="text-right">Angular 8</v-col>
          <v-col cols="8">
            <v-progress-linear value="75"></v-progress-linear>
          </v-col>
        </v-row>
        <v-row align="center">
          <v-col cols="4" class="text-right">Hibernate</v-col>
          <v-col cols="8">
            <v-progress-linear value="88"></v-progress-linear>
          </v-col>
        </v-row>
      </v-col>
      <v-col cols="12" md="6" class="text-center">
        <v-img src="../assets/responsive.svg" aspect-ratio="1.83" contain></v-img>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {};
</script>

<style>
</style>