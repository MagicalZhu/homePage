<script setup lang="ts">
const { t } = useI18n()
</script>

<template>
  <nav class="headerLayout">
    <button :title="t('home.toggle_dark')" @click="toggleDark()">
      <div i="carbon-sun dark:carbon-moon" />
    </button>
  </nav>
</template>

<style scoped>
.headerLayout {
  @apply flex text-xl p-4 md:px-5 top-0 right-0 transition duration-300 absolute
}
</style>
