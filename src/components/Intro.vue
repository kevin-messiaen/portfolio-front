<template>
  <v-container fluid fill-height class="intro-bg">
    <v-layout justify-center align-center fill-height>
      <v-flex text-xs-center class="text-center">
        <p class="display-2 text-center white--text">Freelance Web</p>
        <p class="headline text-center white--text">Des sites rapides et élégants.</p>
        <div class="text-center pt-4 pb-12">
          <v-btn
            ref="button"
            class="ma-2"
            outlined
            color="primary lighten-4"
            @click="$vuetify.goTo(target, options)"
          >à propos de moi</v-btn>
        </div>
      </v-flex>
      <v-btn class="scroll-down ma-2" text icon dark @click="$vuetify.goTo(target, options)">
        <v-icon dark>mdi-chevron-down</v-icon>
      </v-btn>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      target: "#about",
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
.scroll-down {
  position: absolute;
  bottom: 0;
}

.intro-bg {
  background-image: 
    linear-gradient(
      rgba(0, 0, 0, 0.4),
      rgba(0, 0, 0, 0.5)
    ),url("../assets/intro_background.jpg");
  background-repeat: no-repeat;
  background-size: cover;
}

</style>