<script setup>
import sectionOne from "./components/sectionOne.vue";
</script>
<template>
  <div class="parent-all-sections">
    <sectionOne />
  </div>
</template>
<style scoped>
.parent-all-sections {
  @apply md:px-[72px] w-full flex flex-col mt-[200px] xl:mt-[40px] justify-center items-center;
}
</style>
