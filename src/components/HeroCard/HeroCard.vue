<script setup>
const props = defineProps(['hero'])
const showBiography = ref(false)
</script>

<template>
  <div grid class="card">
    <HeroImage :image-url="hero.images.md" @showBiography="showBiography = true" />

    <HeroStats :name="hero.name" :stats="hero.powerstats" :alignment="hero.biography.alignment" />
    <HeroModal v-if="showBiography" @hideBiography="showBiography = false" />
  </div>
</template>

<style scoped>
    .card {
      grid-template-columns: 1fr 1.2fr;
        width: 330px;
        height: 230px;
    }
</style>
