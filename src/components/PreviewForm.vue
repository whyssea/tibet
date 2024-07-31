<script setup lang="ts">
import { ref } from 'vue'
import { SelectProps } from 'ant-design-vue'

const locations = ref<SelectProps['options']>([
  {
    label: 'Локация 1',
    value: '0',
  },
  {
    label: 'Локация 2',
    value: '1',
  },
  {
    label: 'Локация 3',
    value: '2',
  },
])

const participants = ref<SelectProps['options']>([
  {
    label: 'Участник 1',
    value: '0',
  },
  {
    label: 'Участник 2',
    value: '1',
  },
  {
    label: 'Участник 3',
    value: '2',
  },
  {
    label: 'Участник 4',
    value: '3',
  },
])
</script>

<template>
  <a-form class="preview-form__container">
    <a-form-item name="location" class="preview-form__item">
      <a-select
        :options="locations"
        placeholder="Локация для тура"
        class="preview-form__inner-item"
      />
      <p>выберите из списка</p>
    </a-form-item>
    <a-form-item name="date" class="preview-form__item">
      <a-date-picker class="preview-form__inner-item" />
      <p>укажите диапазон</p>
    </a-form-item>
    <a-form-item name="people" class="preview-form__item">
      <a-select
        :options="participants"
        placeholder="Локация для тура"
        class="preview-form__inner-item"
      />
      <p>минимум 4 человека</p>
    </a-form-item>
    <a-form-item class="preview-form__item">
      <a-button html-type="submit" style="width: 213px; font-weight: 700"
        >Найти программу</a-button
      >
    </a-form-item>
  </a-form>
</template>

<style scoped>
.preview-form__container {
  background: rgba(255, 255, 255, 0.2);
  border-radius: 10px;
  display: flex;
  justify-items: stretch;
  gap: 24px;
  padding: 40px;
}
.preview-form__item {
  margin-bottom: 0;
  color: white;
}
.preview-form__inner-item {
  color: white;
  width: 270px;
}
</style>
