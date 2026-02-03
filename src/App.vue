<script setup lang="ts">
import { showToast } from '@nutui/nutui'
const show = () => {
  showToast.text('Hello NutUI Toast!')
};
</script>

<template>
  <div>
    <nut-button type="primary" @click="show">NutUI Button</nut-button>
  </div>
</template>

<style scoped>
</style>
