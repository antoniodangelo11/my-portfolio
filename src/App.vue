<script>
import { RouterLink, RouterView } from 'vue-router';
import { initFlowbite } from "flowbite";
export default {
  created() {
    initFlowbite()
  },
}
</script>

<template>
  <header>
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
    </nav>
  </header>

  <RouterView />
</template>

<style></style>
