<script setup lang="ts">
import ru from 'ant-design-vue/locale/ru_RU'
</script>

<template>
  <a-config-provider
    :locale="ru"
    :theme="{
      token: {
        colorPrimary: 'rgba(26, 62, 62, 1)',
        colorLinkHover: 'rgba(242, 190, 34, 1)',
        colorLinkActive: 'rgba(242, 190, 34, 1)',
        colorLink: 'white',
        fontFamily: 'Inter, system-ui, Avenir, Helvetica, Arial, sans-serif',
        fontSizeHeading2: 32,
      },
      components: {
        Button: {
          borderRadius: 4,
          defaultColor: 'rgba(26, 62, 62, 1)',
          defaultBorderColor: 'rgba(26, 62, 62, 1)',
        },
      },
    }"
    ><slot
  /></a-config-provider>
</template>

<style scoped></style>
