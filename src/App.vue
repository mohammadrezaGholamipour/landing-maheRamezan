<script setup lang="ts">
import Sections from "./components/sections/index.vue";
import Header from "./components/header/index.vue";
</script>
<template>
  <div class="parent-landing">
    <Header />
    <Sections />
  </div>
</template>
<style scoped>
.parent-landing {
  @apply bg-white mx-auto;
  width: clamp(360px, 100%, 1366px);
}
</style>
