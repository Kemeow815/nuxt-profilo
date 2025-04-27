<template>
  <main class="min-h-screen">
    <AppHeader class="mb-8" title="Friends" :description="description" />
    <ul class="grid grid-cols-1 md:grid-cols-2 gap-4">
      <li v-for="bookmark in bookmarks" :key="bookmark.id">
        <a
          :href="bookmark.url"
          target="_blank"
          class="flex items-start gap-3 hover:bg-gray-100 dark:hover:bg-white/10 p-3 rounded-lg transition-colors duration-200"
        >
          <img
            :src="bookmark.image"
            :alt="bookmark.label + ' logo'"
            class="shrink-0 w-12 h-12 rounded-md object-cover border border-gray-200 dark:border-gray-700"
          />
          <div class="flex-1 min-w-0">
            <p class="font-medium truncate text-gray-900 dark:text-gray-100">
              {{ bookmark.label }}
            </p>
            <p class="text-xs text-gray-500 dark:text-gray-400 mt-1 line-clamp-2">
              {{ bookmark.description }}
            </p>
          </div>
          <span class="text-xs font-medium text-gray-400 dark:text-gray-500 shrink-0">
            {{ getHost(bookmark.url) }}
          </span>
        </a>
      </li>
    </ul>
  </main>
</template>

<script setup>
const description = "Some Friends I've met.";
useSeoMeta({
  title: "Friends | Ke Miao",
  description,
});

const bookmarks = [
  {
    id: 1,
    label: "Wallleap",
    url: "https://myblog.wallleap.cn",  // 修复了双斜杠问题
    image: "https://s2.loli.net/2025/04/27/vUPQXSfNrDG6tOI.png", // 图片链接示例
    description: "Luwang's blog",
  },
];

function getHost(url) {
  try {
    const parsedUrl = new URL(url);
    return parsedUrl.host.replace(/^www\./, '');
  } catch {
    return url;
  }
}
</script>
