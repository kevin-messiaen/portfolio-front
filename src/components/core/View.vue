Ò<template>
  <v-content>
    <Intro />
    <About />
    <v-slide-y-reverse-transition>
      <v-btn
        fab
        large
        fixed
        right
        bottom
        color="primary"
        class="ma-4"
        v-show="isNotOnFirstPage"
        @click="$vuetify.goTo(top, options)"
      >
        <v-icon>mdi-chevron-up</v-icon>
      </v-btn>
    </v-slide-y-reverse-transition>
  </v-content>
</template>

<script>
export default {
  components: {
    Intro: () => import("@/components/Intro"),
    About: () => import("@/components/About")
  },
  data() {
    return {
      isNotOnFirstPage: false,
      top: 0,
      options: {
        duration: 300,
        offset: 0,
        easing: "easeInOutCubic"
      }
    };
  },
  methods: {
    handleScroll() {
      this.isNotOnFirstPage = window.scrollY >= window.innerHeight;
    }
  },
  mounted() {
    this.isNotOnFirstPage = window.scrollY >= window.innerHeight;
  },
  created() {
    window.addEventListener("scroll", this.handleScroll);
  },
  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  }
};
</script>

<style>
</style>