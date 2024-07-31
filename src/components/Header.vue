<script setup lang="ts">
const items = [
  {
    label: 'Главная',
    key: 'main',
  },
  {
    label: 'Про гида',
    key: 'guide',
  },
  {
    label: 'Программа тура',
    key: 'program',
  },
  {
    label: 'Стоимость',
    key: 'cost',
  },
  {
    label: 'Блог',
    key: 'blog',
  },
  {
    label: 'Контакты',
    key: 'contacts',
  },
]
</script>

<template>
  <a-flex justify="space-between" align="center" class="header__container">
    <img src="assets/images/logo.svg" alt="Лого" />
    <a-flex justify="stretch">
      <a-flex gap="24" class="header__menu" align="center">
        <a-typography-link v-bind:key="item.key" v-for="item in items">{{
          item.label
        }}</a-typography-link>
      </a-flex>
      <a-button type="primary" class="header__button">Консультация</a-button>
    </a-flex>
  </a-flex>
</template>

<style scoped>
.header__container {
  width: 100%;
}
.header__menu {
  color: white;
  font-weight: 600;
  font-size: 18px;
  margin-right: 50px;
}
.header__button {
  font-weight: 600;
  padding: 10px 24px;
  height: auto;
}
</style>
