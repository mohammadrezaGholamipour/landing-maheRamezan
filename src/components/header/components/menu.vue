<script setup lang="ts">
import { reactive } from "vue";
/////////////////////////////
const state = reactive({
  menuList: [
    { id: 7, name: "پادکس ها" },
    { id: 6, name: "مسابقه کتابخوانی" },
    { id: 5, name: "مناسبت ها" },
    { id: 4, name: "کلیپ ها" },
    { id: 3, name: "عکس نوشته ها" },
    { id: 2, name: "وبینار" },
    { id: 1, name: "فصل بندگی" },
  ],
});
/////////////////////////////
</script>
<template>
  <div class="parent-menu">
    <div v-for="menu in state.menuList" :key="menu.id">
      <p>{{ menu.name }}</p>
      <span class="w-0"></span>
    </div>
  </div>
</template>
<style scoped>
.parent-menu {
  @apply flex justify-center items-center gap-x-[30px];
}
.parent-menu > div {
  @apply flex flex-col justify-between items-end gap-y-[5px] h-[34px] cursor-pointer;
}
.parent-menu P {
  @apply text-[#FFE6B4] text-[18px] whitespace-nowrap;
}
.parent-menu > div:hover span {
  @apply w-full;
}
.parent-menu > div > span {
  @apply transition-all rounded-md h-[2px] duration-300 bg-white;
}
</style>
