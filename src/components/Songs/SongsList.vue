<template>
  <div class="song-card">
      <div class="song-card_element">
        <div class="song-card_left">
        <button>Play</button>
        <p>image</p>
      </div>
        <div class="song-card_info">  
          <p><!--{{ song.title }}-->song</p>
          <p>artist</p>
        </div>
      </div>
      <div class="song-card_right">
        <p><!--{{ song.duration }}-->00:00</p>
      </div>
  </div>
</template>
  
  <script>
  
  </script>
  
  <style lang="scss" scoped>
  .song-card {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    color: black;
    width: 350px;
    border-radius: 5px;
    background-color: white;
    border: 0,5px solid black;
    padding: 15px;
    margin-top: 30px;

    &_element {
      display: flex;
      flex-direction: row;
    }

    &_left {
      display: flex;
      flex-direction: row;
      align-items: center;
    }

    &_info {
      display: flex;
      flex-direction: column;
      align-items: center;
      padding-left: 30px;
    }

    &_right {
      display: flex;
      flex-direction: row;
      align-items: center;
    }
  }
  </style>
  