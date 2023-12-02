<script lang="ts"></script>
<template>
  <div class="parent-section">
    <div class="parent-btns">
      <button>
        <p>وبینارها</p>
      </button>
      <button>
        <p>عکس نوشته</p>
      </button>
      <button>
        <p>کلیپ ها</p>
      </button>
      <button>
        <p>شرکت در پویش</p>
      </button>
    </div>
    <img class="hidden xl:flex" src="@/assets/images/section-one-larg.svg" />
    <img class="flex xl:hidden" src="@/assets/images/section-one-small.svg" />
  </div>
</template>
<style scoped>
.parent-section {
  @apply w-full flex flex-col justify-center gap-[20px] xl:items-end items-center;
}
.parent-btns {
  @apply flex flex-wrap justify-center items-center gap-[20px];
}
button {
  @apply flex shadow-sm p-3 whitespace-nowrap justify-center items-center bg-[#07023B] rounded-[5px];
  all: inset;
}
button p {
  @apply text-white text-[18px];
}
</style>
