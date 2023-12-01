<script setup lang="ts">
import Menu from "./components/menu.vue";
</script>
<template>
  <div class="parent-header">
    <!-- /////////////////////// -->
    <div class="header-top">
      <img src="@/assets/images/header-one.svg" />
      <Menu />
    </div>
    <!-- /////////////////////// -->
    <div class="header-bottom">
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
        <img class="self-start" src="@/assets/images/header-three.svg" />
      </div>
      <img class="top-[-75px] relative" src="@/assets/images/header-two.svg" />
    </div>
    <!-- /////////////////////// -->
  </div>
</template>
<style scoped>
.parent-header {
  @apply relative w-full h-[570px] pt-[40px] bg-[#0D0870] rounded-b-[40px] px-[72px];
}
.header-top {
  @apply w-full justify-between flex items-start gap-[20px];
}
.header-bottom {
  @apply flex justify-between items-start;
}
.header-bottom > div {
  @apply flex flex-col items-end text-right justify-center gap-y-[10px] text-white;
}
.header-bottom > div > p:first-child {
  @apply font-[dana] text-[47px] text-[#FFE6B4];
}
</style>
