<script setup lang="ts">
const { t, availableLocales, locale } = useI18n()

const toggleLocales = () => {
  // change to some real logic
  const locales = availableLocales
  locale.value = locales[(locales.indexOf(locale.value) + 1) % locales.length]
}
</script>

<template>
  <nav text-xl mb-6>
    <a class="icon-btn mx-2" href="https://www.huakucha.top" :title="t('button.home')" target="_blank">
      <div i-carbon:notebook />
    </a>

    <a class="icon-btn mx-2" href="https://blog.huakucha.top" :title="t('button.about')">
      <div i-carbon:text-annotation-toggle />
    </a>

    <button class="icon-btn mx-2 !outline-none" :title="t('button.toggle_dark')" @click="toggleDark()">
      <div i="carbon-sun dark:carbon-moon" />
    </button>

    <a class="icon-btn mx-2" rel="noreferrer" href="https://github.com/MagicalZhu" target="_blank" title="GitHub">
      <div i-carbon-logo-github />
    </a>
  </nav>
</template>
