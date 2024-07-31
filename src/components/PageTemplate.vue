<script setup lang="ts">
const props = defineProps<{
  gray?: boolean
}>()
</script>

<template>
  <a-flex
    :style="{
      margin: '80px 0 100px 0',
      background: props.gray ? 'rgba(243, 245, 244, 1)' : 'white',
    }"
  >
    <slot></slot>
  </a-flex>
</template>

<style scoped></style>
