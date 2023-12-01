<script setup lang="ts">
import Header from "./components/header/index.vue";
</script>
<template>
  <div class="parent-landing">
    <Header />
  </div>
</template>
<style scoped>
.parent-landing {
  @apply bg-white mx-auto;
  width: clamp(360px, 100%, 1366px);
}
</style>
