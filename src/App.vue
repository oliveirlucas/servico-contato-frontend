<template>
  <div class="background" >
    <v-app>
      <div>
        <v-img
          width=""
          src="./assets/naometoc.jpg"
        ></v-img>
      </div>
      <v-main>
        <Menu />
      </v-main>
    </v-app>
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Menu from "./components/Menu.vue";

export default Vue.extend({
  name: "App",

  components: {
    Menu
  },
});
</script>

<style>
</style>
