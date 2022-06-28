<script setup lang="ts">
// const user = useUserStore()
// const { t } = useI18n()
</script>

<template>
  <div class="h-8 w-full bg-white" />
  <header class="flex text-primary">
    <div class="p-32">
      <h1 class="farbod text-4xl mb-4">
        رادیو آپ‌استریم
      </h1>
      <p class="farbod text-lg mb-4">
        پادکستی درباره مهندسی نرم‌افزار، تلاشی بی‌پایان برای ساده‌سازی پیچیدگی‌ها
      </p>
      <p class="farbod">
        توسط مهدی کریمی
      </p>
    </div>
    <div class="h-175 overflow-hidden">
      <img class="grayscale" src="mahdi-karimi.jpg" alt="">
    </div>
  </header>
  <div class="h-8 w-full bg-white" />
  <main>
    <section class=" px-32">
      <h2 class="my-8 text-2xl text-primary farbod">
        جدیدترین اپیزودها
      </h2>
      <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
        <ui-pocast-item v-for="i in 11" :key="i" :thumbnail="`https://picsum.photos/id/${i}/1000?grayscale`" :slug="String(i)" />
      </div>
    </section>
  </main>
  <footer>
    {{ new Date().getFullYear() }}
  </footer>
</template>

<route lang="yaml">
meta:
  layout: home
</route>
