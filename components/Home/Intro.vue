<template>
  <div class="space-y-6">
    <NuxtImg src="/avatar.png" alt="克喵爱吃卤面"
      class="ring-2 border ring-gray-200 border-gray-300 dark:ring-white/10 dark:border-gray-800 hover:ring-4 transition-all duration-300 bg-gray-200 dark:bg-gray-900 rounded-full h-12 w-12 sm:h-16 sm:w-16"
      sizes="48px sm:64px" placeholder format="webp" />
    <h1 class="text-xl font-bold tracking-tight text-gray-800 dark:text-gray-100">
      Hello!
    </h1>
    <p class="text-gray-900 dark:text-gray-400">
      我是克喵爱吃卤面，在南京就读的大二学生，双非二本的自动化牛马。<br />
      资源分享者 / 博主 / 学生
    </p>
    <p class="text-gray-900 dark:text-gray-400">
      我的学校是
      <a href="https://www.niit.edu.cn" target="_blank" class="underline">南京工业职业技术大学</a>, 致力于
      分享开源项目、网站、实用软件等等，记录我的日常生活和踩坑教程。
      希望您能在我这里得到您想要的。
    </p>
  </div>
</template>

<script setup>
useSeoMeta({
  title: "克喵爱吃卤面",
  description:
    "我是克喵爱吃卤面，在南京就读的大二学生，双非二本的自动化牛马。",
});
</script>
