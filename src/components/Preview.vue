<script setup lang="ts"></script>

<template>
  <a-flex vertical class="preview__container" justify="space-between">
    <Header />
    <div>
      <a-typography-title :level="1" class="preview__title">{{
        `Насладись прогулкой в горах
с командой единомышленников`.toUpperCase()
      }}</a-typography-title>
      <PreviewForm class="preview__form" />
      <a-button size="large" class="preview__button">Найти программу</a-button>
    </div>
  </a-flex>
</template>

<style scoped>
.preview__container {
  width: 100%;
  max-width: 1180px;
  height: 100vh;
  margin: 0 auto;
  padding: 16px 16px 82px 16px;
}
.preview__title {
  color: white;
  font-weight: 700;
  white-space: pre-wrap;
  margin-bottom: 41px;
}
.preview__form {
  display: flex;
}
.preview__button {
  display: none;
}
@media screen and (max-width: 900px) {
  .preview__container {
    padding: 20px 16px 50px 16px;
  }
  .preview__title {
    font-size: 28px;
    line-height: 42px;
  }
  .preview__form {
    display: none;
  }
  .preview__button {
    display: block;
  }
}
</style>
