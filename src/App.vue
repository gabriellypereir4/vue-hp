<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
import HelloWorld from "./components/HelloWorld.vue";
</script>

<template>
  <header>
    <nav class="wrapper">
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/personagens">Personagens</RouterLink>
    </nav>
  </header>

  <div id="content">
    <RouterView />
  </div>
</template>

<style scoped>
nav {
  display: flex;
  gap: 10px;
}
header {
  display: flex;
  flex-wrap: wrap;
}
.content {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
