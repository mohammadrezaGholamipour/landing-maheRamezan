<script setup lang="ts"></script>
<template>
  <div class="parent-section">
    <!-- /////////////////////////// -->
    <div class="section-content">
      <img src="@/assets/images/section-two-one.svg" />
      <img src="@/assets/images/section-two-three.svg" />
      <p>
        لورم ایپسوم متن ساختگی با تولید سادگی نامفهوم از صنعت چاپ، و با استفاده
        از طراحان گرافیک است، چاپگرها و متون بلکه روزنامه و مجله در ستون و
        سطرآنچنان که لازم است، و برای شرایط فعلی تکنولوژی مورد نیاز، و کاربردهای
        متنوع با هدف بهبود ابزارهای کاربردی می باشد، کتابهای زیادی در شصت و سه
        درصد گذشته حال و آینده، شناخت فراوان جامعه و متخصصان را می طلبد، تا با
        نرم افزارها شناخت بیشتری را برای طراحان رایانه ای علی الخصوص طراحان
        خلاقی، و فرهنگ پیشرو در زبان فارسی ایجاد کرد، در این صورت می توان امید
        داشت که تمام و دشواری موجود در ارائه راهکارها، و شرایط سخت تایپ به پایان
        رسد و زمان مورد نیاز شامل حروفچینی دستاوردهای اصلی، و جوابگوی سوالات
        پیوسته اهل دنیای موجود طراحی اساسا مورد استفاده قرار گیرد
      </p>
      <p>زمان بندی وبینار ها</p>
      <div class="section-content-list">
        <div v-for="item in 10" :key="item">
          <div>
            <img width="23" src="@/assets/images/section-two-two.png" />
            <p>استاد ابوالحسینی</p>
          </div>
          <p>1402/9/11</p>
          <p>15:00</p>
          <button><p>شرکت در دوره</p></button>
        </div>
      </div>
    </div>
    <!-- ////////////////////////// -->
    <img src="@/assets/images/section-two-four.svg" />
    <!-- ////////////////////////// -->
  </div>
</template>
<style scoped>
.parent-section {
  @apply w-full relative flex justify-start items-center;
}
.section-content {
  @apply w-full xl:w-[86%] relative flex flex-col gap-[15px] items-start justify-center bg-[#F6F5FF] border border-[#0D0870] rounded-[15px] p-[40px] pt-[60px];
}
.section-content > img:nth-child(1) {
  @apply absolute top-[-38px] right-[50px];
}
.section-content > img:nth-child(2) {
  @apply absolute bottom-[-150px] right-[-100px];
}
.parent-section > img {
  @apply absolute hidden xl:flex left-[-50px] bottom-0;
}
.section-content > p:nth-child(4) {
  @apply text-[23px] font-[dana] font-bold;
}
.section-content-list {
  @apply flex w-full xl:w-[75%] flex-col h-[270px] overflow-auto p-[10px] items-start justify-start gap-[15px];
}
.section-content-list > div {
  @apply w-full flex items-center justify-between gap-x-[60px] whitespace-nowrap;
}
.section-content-list > div > p {
  @apply text-[16px];
}
.section-content-list > div > div {
  @apply flex items-center justify-start gap-x-[10px];
}
.section-content-list > div > div > p {
  @apply text-[18px];
}
button {
  @apply flex transition-all shadow-sm p-3 px-4 whitespace-nowrap border-[#07023B] border-2 justify-center items-center bg-[#07023B] rounded-[5px];
  all: inset;
}
button:hover {
  @apply bg-white text-black;
}
button:hover p {
  @apply text-black;
}
button p {
  @apply text-white transition-all text-[18px];
}
</style>
