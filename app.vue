<script setup lang="ts">
useHead({
  meta: [
    { name: 'viewport', content: 'width=device-width, initial-scale=1' }
  ],
  link: [
    { rel: 'icon', href: '/favicon.ico' }
  ],
  htmlAttrs: {
    lang: 'pt-br'
  }
})

useSeoMeta({
  ogImage: 'https://i.imgur.com/mu5gbbY.png',
  twitterImage: 'https://i.imgur.com/mu5gbbY.png',
  twitterCard: 'summary_large_image'
})
</script>

<template>
  <Header />

  <UMain>
    <NuxtPage />
  </UMain>

  <Footer />

  <UNotifications />
</template>
