<template>
  <v-app>
    <v-main>
      <Auth />
    </v-main>
  </v-app>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import Auth from "./components/Auth.vue";

@Options({
  components: {
    Auth,
  },
})
export default class App extends Vue {}
</script>
