<script setup lang="ts">
import { showDialog } from '@nutui/nutui'
import { ref } from 'vue'
let showPopup = ref(false)
const show = () => {
  showPopup.value = true
};
const toShowDialog = () => {
  showDialog({
    content: `温馨提示`,
    okText: '关闭',
    noCancelBtn: true,
    closeOnPopstate: true,
  })
};
</script>

<template>
  <nut-cell title="Click to show Popup" is-link @click="show"></nut-cell>
  <nut-popup v-model:visible="showPopup" position="bottom" closeable round teleport-disable style="height: 50vh">
    <div style="display: flex; justify-content: center; flex-direction: column; height: 50vh; align-items: center;">
      <div>因为业务原因，这里需要是个弹窗</div>
      <div>这个弹窗实际上不是半屏而是全屏，表现为Dialog不可见</div>
      <div>这里为了更直观一点，改为半屏</div>
      <nut-button type="primary" @click="toShowDialog">showDialog</nut-button>
    </div>
  </nut-popup>
</template>

<style scoped>
</style>
