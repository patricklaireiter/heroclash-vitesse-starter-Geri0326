<script setup>
const emits = defineEmits(['hideBiography'])
</script>

<template>
  <div class="modal" @click="emits('hideBiography')" />
</template>

<style scoped>
.modal{

    position: fixed;
    top:0;
    left:0;
    z-index: 1;
    width: 100vw;
    height: 100vh;
    background-color: rgba(0, 255, 234, 0.37);
}
</style>
