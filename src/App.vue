<script setup lang="ts">
// https://github.com/vueuse/head
// you can use this to manipulate the document head in any components,
// they will be rendered correctly in the html results with vite-ssg
useHead({
  title: 'Athu Home',
  meta: [
    { name: 'description', content: 'Athu Home Site' },
    {
      name: 'theme-color',
      content: computed(() => isDark.value ? '#818CF8' : '#ffffff'),
    },
  ],
  link: [
    {
      rel: 'icon',
      type: 'image/svg+xml',
      href: '/favicon.svg',
    },
  ],
})
</script>

<template>
  <RouterView />
</template>
