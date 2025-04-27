<template>
  <div>
    <h2 class="uppercase text-xs font-semibold text-gray-400 mb-4">FIND ME ON</h2>
    <div class="space-y-5">
      <NuxtLink
        v-for="link in links"
        :key="link.icon"
        :to="link.url"
        target="_blank"
        external
        class="flex items-end gap-4 dark:hover:text-gray-300 group"
      >
        <span class="text-sm">
          {{ link.name }}
        </span>
        <div
          class="flex-1 border-b border-dashed border-gray-300 dark:border-gray-800 group-hover:border-gray-700"
        ></div>
        <Icon :name="link.icon" class="w-6 h-6"></Icon>
      </NuxtLink>
    </div>
  </div>
</template>

<script lang="ts" setup>
const links = [
  {
    name: "Twitter",
    url: "https://twitter.com/kemiaosw",
    icon: "mdi:twitter",
  },
  {
    name: "GitHub",
    url: "https://github.com/Kemeow815",
    icon: "mdi:github",
  },
  {
    name: "Mail",
    url: "mailto:kemiaofx@163.com",
    icon: "mdi:mail",
  },
  {
    name: "BiliBili",
    url: "https://space.bilibili.com/3546643173477234",
    icon: "mdi:television-classic",
  },
  {
    name: "Telegram",
    url: "https://t.me/KemiaoJun",
    icon: "mdi:telegram",
  },
];
</script>
