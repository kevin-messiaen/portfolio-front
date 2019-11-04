<template>
  <v-app>
    <CoreToolbar />
    <CoreView />
    <CoreFooter />
  </v-app>
</template>

<script>
export default {
  name: "App",
  components: {
    CoreToolbar: () => import("@/components/core/Toolbar"),
    CoreView: () => import("@/components/core/View"),
    CoreFooter: () => import("@/components/core/Footer")
  }
};
</script>