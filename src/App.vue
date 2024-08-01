<script setup lang="ts">
import AntdProvider from 'providers/AntdProvider.vue'
</script>

<template>
  <AntdProvider>
    <a-flex vertical align="center">
      <div class="container">
        <Preview />
      </div>
      <About />
      <Programs />
      <PopularRoutes />
      <Blog />
    </a-flex>
  </AntdProvider>
</template>

<style scoped>
.container {
  width: 100%;
  background-image: url('assets/images/header-bg.png');
  background-repeat: no-repeat;
  background-size: cover;
}
</style>
