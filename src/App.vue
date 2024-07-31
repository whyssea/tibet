<script setup lang="ts">
import AntdProvider from 'providers/AntdProvider.vue'
</script>

<template>
  <AntdProvider>
    <div class="container">
      <Preview />
    </div>
  </AntdProvider>
</template>

<style scoped>
.container {
  background-image: url('assets/images/header-bg.png');
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
