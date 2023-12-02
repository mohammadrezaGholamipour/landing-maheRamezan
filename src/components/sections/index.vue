<script setup>
import sectionOne from "./components/sectionOne.vue";
import sectionTwo from "./components/sectionTwo.vue";
</script>
<template>
  <div class="parent-all-sections">
    <sectionOne />
    <sectionTwo />
  </div>
</template>
<style scoped>
.parent-all-sections {
  @apply md:px-[72px] px-[15px] w-full flex flex-col mt-[200px] xl:mt-[40px] gap-y-[50px] justify-center items-center;
}
</style>
