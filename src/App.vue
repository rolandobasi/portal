<template>
  <v-app>
    <nabVar />
    <v-content>
      <router-view />
    </v-content>
  </v-app>
</template>

<script>
import { defineAsyncComponent } from "vue";
export default {
  name: "App",
  components: {
    nabVar: defineAsyncComponent(() =>
      import("@/components/global/NabVar.vue")
    ),
  },
};
</script>
