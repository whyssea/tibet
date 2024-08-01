<script setup lang="ts"></script>

<template>
  <a-flex vertical class="preview__container" justify="space-between">
    <Header />
    <div>
      <a-typography-title :level="1" class="preview__title">{{
        `Насладись прогулкой в горах
с командой единомышленников`.toUpperCase()
      }}</a-typography-title>
      <PreviewForm />
    </div>
  </a-flex>
</template>

<style scoped>
.preview__container {
  width: 1180px;
  height: 100vh;
  margin: 0 auto;
  padding: 16px 0 82px 0;
}
.preview__title {
  color: white;
  font-weight: 700;
  white-space: pre-wrap;
  margin-bottom: 41px;
}
</style>
