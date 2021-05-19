<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <Menu />
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Menu from "@/components/Menu.vue";

@Component({
  components: {
    Menu
  }
})
export default class Home extends Vue {}
</script>
