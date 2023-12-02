<script setup lang="ts">
import { reactive } from "vue";
import Menu from "./components/menu.vue";
/////////////////////////////////////////
const state = reactive({
  menuMobileStatus: false,
});
////////////////////////////////
const handleChangeMenuMobileStatus = (status:boolean) => {
  state.menuMobileStatus = status;
};
</script>
<template>
  <div class="parent-header">
    <!-- /////////////////////// -->
    <div class="header-top">
      <Menu
        @change-menu-mobile-status="handleChangeMenuMobileStatus"
        :menuMobileStatus="state.menuMobileStatus"
      />
      <img class="hidden xl:flex" src="@/assets/images/header-one-larg.svg" />
      <img class="flex xl:hidden" src="@/assets/images/header-one-small.svg" />
    </div>
    <!-- /////////////////////// -->
    <div class="header-bottom">
      <img
        class="hidden xl:flex top-[-75px] relative"
        src="@/assets/images/header-two-larg.svg"
      />
      <img
        class="flex xl:hidden top-[-55px] relative"
        src="@/assets/images/header-two-small.svg"
      />
      <div>
        <p>فصل بندگی</p>
        <p>
          لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ، و با
          استفاده از طراحان گرافیک است، چاپگرها و متون بلکه روزنامه و مجله در
          ستون و سطرآنچنان که لازم است، و برای شرایط فعلی تکنولوژی مورد نیاز، و
          کاربردهای متنوع با هدف بهبود ابزارهای کاربردی می باشد، کتابهای زیادی
          در شصت و سه درصد گذشته حال و آینده، شناخت فراوان جامعه و متخصصان را می
          طلبد، تا با نرم افزارها شناخت بیشتری را برای طراحان
        </p>
        <img class="self-end" src="@/assets/images/header-three.svg" />
      </div>
    </div>
    <!-- /////////////////////// -->
  </div>
</template>
<style scoped>
.parent-header {
  @apply flex flex-col w-full h-[570px] bg-[#0D0870] rounded-b-[40px] p-[15px] md:py-[40px] md:px-[72px] gap-y-[30px] md:gap-0;
}
.header-top {
  @apply w-full justify-between flex items-center md:items-start gap-[20px];
}
.header-bottom {
  @apply flex flex-col-reverse xl:flex-row justify-between items-center xl:items-start;
}
.header-bottom > div {
  @apply flex flex-col items-start text-right justify-center gap-y-[10px] text-white;
}
.header-bottom > div > p:first-child {
  @apply font-[dana] text-[47px] text-[#FFE6B4];
}
</style>
