<template>
  <v-app>
    <CoreToolbar />
    <CoreView />
  </v-app>
</template>

<script>
export default {
  name: "App",
  components: {
    CoreToolbar: () => import("@/components/core/Toolbar"),
    CoreView: () => import("@/components/core/View")
  }
};
</script>