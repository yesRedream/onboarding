<template>
  <div class="main-layout">
    <BaseHeader></BaseHeader>
    <div class="main-layout__content">
      <Orders></Orders>
    </div>
  </div>
</template>

<script>
  import BaseHeader from './base/BaseHeader.vue';
  import Orders from '../pages/orders/index.vue';

  export default {
    name: 'MainLayout',
    components: {
      BaseHeader,
      Orders
    },
  }
</script>

<style scoped>
  .main-layout__content {
    min-height: calc(100vh - 60px);
    background: #EEF0F4;
  }
</style>
