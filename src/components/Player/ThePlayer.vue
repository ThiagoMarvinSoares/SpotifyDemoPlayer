<template>
  <div class="player-card">
    <div class="player-card_left">
      <div>
        <p>image</p>
      </div>
      <div class="player-card_info">  
        <p><!--{{ song.title }}-->song</p>
        <p>artist</p>
      </div>
    </div>
    <div class="player-element">
      <p>player</p>
    </div>
    <div class="player-volume">
      <p>volume</p>
    </div>
  </div>      
  </template>
  
  <script>
  </script>
  
<style scoped>
  .player-card {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    bottom: 0;
    position: fixed;
     /* colors and styles */
    color: white;
    background-color: black;
    width: 100%;
  }
  .player-card_left {
      display: flex;  
      flex-direction: row;
    }

</style>
  