<script setup lang="ts">
useHead({
  meta: [{ name: "viewport", content: "width=device-width, initial-scale=1" }],
  link: [{ rel: "icon", href: "/logo.ico" }],
  htmlAttrs: {
    lang: "pl",
  },
});

useSeoMeta({
  ogImage: "https://i.ibb.co/fF0Ws4T/logo.jpg",
  twitterImage: "https://i.ibb.co/fF0Ws4T/logo.jpg",
  twitterCard: "summary_large_image",
});
</script>

<template>
  <Header />

  <UMain>
    <NuxtPage />
  </UMain>

  <Footer />
  <UNotifications />
</template>
