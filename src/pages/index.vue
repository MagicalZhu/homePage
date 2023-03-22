<script setup lang="ts">
const { t } = useI18n()
</script>

<template>
  <div class="flex flex-col items-center min-h-[calc(80vh-44px)] justify-center">
    <div text-6xl>
      <div i-carbon:fingerprint-recognition inline-block text-red-200 />
    </div>
    <!--
      <p text-2xl mt-1>
        Athu
      </p>
    -->
    <p text-base opacity-45 mt-1>
      {{ t('intro.desc') }}
    </p>
    <nav text-xl mt-6>
      <a class="icon-btn mx-2" href="https://www.huakucha.top" :title="t('home.wiki')" target="_blank">
        <div i-carbon:notebook />
      </a>

      <a class="icon-btn mx-2" href="https://blog.huakucha.top" :title="t('home.blog')" target="_blank">
        <div i-carbon:text-annotation-toggle />
      </a>

      <button class="icon-btn mx-2 !outline-none" :title="t('home.toggle_dark')" @click="toggleDark()">
        <div i="carbon-sun dark:carbon-moon" />
      </button>

      <a class="icon-btn mx-2" rel="noreferrer" href="https://github.com/MagicalZhu" target="_blank" title="GitHub">
        <div i-carbon-logo-github />
      </a>
    </nav>
  </div>
</template>

<route lang="yaml">
meta:
  layout: home
</route>
