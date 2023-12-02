<script setup lang="ts">
import { reactive } from "vue";
/////////////////////////////
const props = defineProps<{ menuMobileStatus: boolean }>();
const emit = defineEmits<{ changeMenuMobileStatus: [boolean] }>();
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
  <div class="parent-menu z-[9999]">
    <!-- /////////////////////// -->
    <div class="menu-system">
      <div v-for="menu in state.menuList" :key="menu.id">
        <p>{{ menu.name }}</p>
        <span class="w-0"></span>
      </div>
    </div>
    <!-- /////////////////////// -->
    <div @click="emit('changeMenuMobileStatus', true)" class="btn-menu">
      <p>منو</p>
      <img src="@/assets/images/menu-btn.svg" />
    </div>
    <!-- /////////////////////// -->
    <transition-slide>
      <div v-if="props.menuMobileStatus" class="menu-mobile">
        <div>
          <p v-for="menu in state.menuList" :key="menu.id">{{ menu.name }}</p>
        </div>
        <img
          @click="emit('changeMenuMobileStatus', false)"
          src="@/assets/images/close-menu.svg"
        />
      </div>
    </transition-slide>
    <!-- /////////////////////// -->
  </div>
</template>
<style scoped>
.menu-system {
  @apply hidden xl:flex justify-center items-center gap-x-[30px];
}
.menu-system > div {
  @apply flex flex-col justify-between items-start gap-y-[5px] h-[34px] cursor-pointer;
}
.parent-menu P {
  @apply text-[#FFE6B4] text-[18px] whitespace-nowrap;
}
.menu-system > div > span {
  @apply transition-all rounded-md h-[2px] duration-300 bg-white;
}
.menu-system > div:hover span {
  @apply w-full;
}
.btn-menu {
  @apply flex xl:hidden items-center gap-x-[10px];
}
.btn-menu p {
  @apply text-[20px] font-bold;
}
.menu-mobile {
  @apply fixed flex flex-col justify-start gap-y-[10px] items-center overflow-hidden top-0 left-0 w-screen h-screen backdrop-blur-sm;
}
.menu-mobile > div {
  @apply flex w-full flex-col-reverse gap-y-[10px] py-5 rounded-b-xl border-2 border-t-0  justify-center items-center bg-[#0D0870];
}
.menu-mobile p,
img {
  @apply cursor-pointer;
}
</style>
