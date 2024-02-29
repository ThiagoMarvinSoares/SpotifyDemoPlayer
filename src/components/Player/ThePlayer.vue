<template>
  <div class="wrap">
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
  </div>
  
  </template>
  
  <script>
  </script>
  
<style scoped>
.wrap {
  width: 100%;
  height: 100%;
  display: flex;
  justify-content: center;
  align-items: center;
}
.player-card {
    display: flex;
    flex-direction: row;
    justify-content: space-around;
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

    .player-element {
      margin-right: 40px;
    }  

</style>
  