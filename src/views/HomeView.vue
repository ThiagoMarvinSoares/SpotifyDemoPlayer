<script setup>
import SongsList from '../components/Songs/SongsList.vue'
import ThePlayer from '../components/Player/ThePlayer.vue'
</script>

<template>
  <main class="app-elements">
    <SongsList />
    <ThePlayer />
  </main>
</template>

<style>
  .app-elements {
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 100vh;
  }
</style>