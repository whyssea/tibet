<script setup lang="ts">
const props = defineProps<{
  preTitle: string
  title: string
}>()
</script>

<template>
  <p class="blockTitle__pre">{{ props.preTitle }}</p>
  <a-typography-title :level="2" class="blockTitle__title">{{
    props.title
  }}</a-typography-title>
</template>

<style scoped>
.blockTitle__pre {
  color: rgba(242, 190, 34, 1);
  font-size: 24px;
  line-height: 20px;
  margin-bottom: 8px;
}
.blockTitle__title {
  margin-bottom: 40px;
  font-weight: 800;
}
</style>
