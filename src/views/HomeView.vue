<script setup>
import SongsList from '../components/Songs/SongsList.vue'
import ThePlayer from '../components/Player/ThePlayer.vue'
import SpotifyAPI from '../components/SpotifyAPI/Spotify.vue'
</script>

<template>
  <main class="app-elements">
    <SongsList />
    <ThePlayer />
    <SpotifyAPI />
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