<script setup lang="ts">
const { t } = useI18n()
</script>

<template>
  <div class="flex flex-col items-center min-h-[calc(90vh-44px)] justify-center">
    <div class="text-8em">
      <div i-carbon:fingerprint-recognition inline-block text-red-200 dark:text-indigo-300 />
    </div>
    <!--
      <p text-base opacity-45 mt-1>
      {{ t('intro.desc') }}
      </p>
    -->
    <nav mt-6 grid class="gridLayout">
      <div font-mono text-lg text-gray-400>
        <div py-5 font-italic>
          Write:
        </div>
        <div py-5 font-italic>
          Social:
        </div>
      </div>
      <div grid grid-cols-3 text-center>
        <a class="icon-btn" href="https://wiki.huakucha.top" :title="t('home.wiki')" target="_blank">
          <div i-line-md:text-box />
        </a>
        <a class="icon-btn" href="https://blog.huakucha.top" :title="t('home.blog')" target="_blank">
          <div i-line-md:edit />
        </a>
        <div />
        <!-- social -->
        <a class="icon-btn" rel="noreferrer" href="https://github.com/MagicalZhu" target="_blank" title="GitHub">
          <div i-line-md:github />
        </a>
        <a class="icon-btn" rel="noreferrer" href="https://m.cmx.im/@athu" target="_blank" title="Mastodon">
          <div i-line-md:mastodon />
        </a>
        <a class="icon-btn" rel="noreferrer" href="mailto:huakucha95@163.com" target="_blank" title="Email">
          <div i-line-md:email />
        </a>
      </div>
    </nav>
  </div>
</template>

<style scoped>
.icon-btn {
  @apply  text-3xl text-gray-300 cursor-pointer select-none  transition duration-100 ease-in-out pointer-events-auto rounded-md p-3;
  @apply hover:text-indigo-200;
  @apply focus-visible:outline-none focus-visible:ring-2 focus-visible:ring-white focus-visible:ring-opacity-50;
}
.gridLayout {
  grid-template-columns: 40% 60%;
}
</style>

<route lang="yaml">
meta:
  layout: home
</route>
