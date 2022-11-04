<script setup>
const props = defineProps(['hero'])
function showBiography() {
  alert('Hi')
}
</script>

<template>
  <div grid class="card">
    <HeroImage :image-url="hero.images.md" @showBiography="showBiography" />

    <HeroStats :name="hero.name" :stats="hero.powerstats" :alignment="hero.biography.alignment" />
  </div>
</template>

<style scoped>
    .card {
      grid-template-columns: 1fr 1.2fr;
        width: 330px;
        height: 230px;
    }
</style>
