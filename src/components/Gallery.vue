<script setup lang="ts">
import ph1 from 'assets/images/gallery/ph1.png'
import ph2 from 'assets/images/gallery/ph2.png'
import ph3 from 'assets/images/gallery/ph3.png'
import ph4 from 'assets/images/gallery/ph4.png'
</script>

<template>
  <PageTemplate>
    <a-flex vertical align="center" class="gallery__container">
      <BlockTitle title="Делимся впечатлениями" pre-title="фото-отчет" />
      <div>
        <a-row :gutter="20" style="margin-bottom: 20px">
          <a-col :span="12"><a-image :src="ph1" /></a-col>
          <a-col :span="6"><a-image :src="ph2" /></a-col>
          <a-col :span="6"><a-image :src="ph3" /></a-col>
        </a-row>
        <a-row :gutter="20">
          <a-col :span="6"><a-image :src="ph4" /></a-col>
          <a-col :span="12"><a-image :src="ph1" /></a-col>
          <a-col :span="6"><a-image :src="ph2" /></a-col>
        </a-row>
      </div>
      <a-button type="primary" style="margin-top: 50px">Наш pinterest</a-button>
    </a-flex>
  </PageTemplate>
</template>

<style scoped>
.gallery__container {
  max-width: 1180px;
  margin: 0 auto;
}
</style>
