<script setup lang="ts">
import { ref } from 'vue'
import menuIcon from 'assets/images/menu-icon.svg'
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
const open = ref<boolean>(false)
const showDrawer = () => {
  open.value = true
}
</script>

<template>
  <a-flex justify="space-between" align="center" class="header__container">
    <img class="header__icon" src="assets/images/logo.svg" alt="Лого" />
    <a-flex justify="stretch" class="header__menu">
      <a-flex gap="24" align="center" style="margin-right: 50px">
        <a-typography-link v-bind:key="item.key" v-for="item in items">{{
          item.label
        }}</a-typography-link>
      </a-flex>
      <a-button type="primary" class="header__button">Консультация</a-button>
    </a-flex>
    <div @click="showDrawer" class="header__menu-button">
      <img :src="menuIcon" alt="Меню" />
    </div>
    <a-drawer
      v-model:open="open"
      placement="right"
      style="background-color: rgba(26, 62, 62, 1)"
    >
      <a-flex :gap="16" vertical>
        <a-typography-link v-bind:key="item.key" v-for="item in items"
          >> {{ item.label }}</a-typography-link
        >
      </a-flex>
    </a-drawer>
  </a-flex>
</template>

<style scoped>
.header__container {
  width: 100%;
}
.header__icon {
  width: 137px;
  object-fit: contain;
}
.header__menu {
  color: white;
  font-weight: 600;
  font-size: 18px;
}
.header__button {
  font-weight: 600;
  padding: 10px 24px;
  height: auto;
}
.header__menu-button {
  display: none;
}
.header__menu-button:hover {
  cursor: pointer;
}
@media screen and (max-width: 900px) {
  .header__icon {
    width: 84px;
  }
  .header__button {
    display: none;
  }
  .header__menu {
    display: none;
  }
  .header__menu-button {
    display: block;
  }
}
</style>
