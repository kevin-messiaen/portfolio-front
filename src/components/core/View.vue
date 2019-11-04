Ò<template>
  <v-content>
    <v-container fluid class="pa-0">
      <Intro />
      <About />
      <Contact />
    </v-container>
  </v-content>
</template>

<script>
export default {
  components: {
    Intro: () => import("@/components/Intro"),
    About: () => import("@/components/About"),
    Contact: () => import("@/components/Contact")
  }
};
</script>

<style>
</style>