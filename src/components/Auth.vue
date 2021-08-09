<template>
  <v-btn flat @click="auth">Connect wallet</v-btn>
</template>

<script lang="ts">
import { Vue } from "vue-class-component";
import { AppConfig, showConnect, UserSession } from "@stacks/connect";

export default class Auth extends Vue {
  public auth() {
    let appConfig = new AppConfig(["store_write", "publish_data"]);
    let userSession = new UserSession({ appConfig });
    console.info(userSession,appConfig)

    showConnect({
      appDetails: {
        name: 'MyApp',
        icon: '',
      },
      onCancel: () => {
        console.error("CANCEL!!!")
      }
    });
  }
}
</script>
