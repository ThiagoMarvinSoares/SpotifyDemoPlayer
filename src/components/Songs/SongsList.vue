<template>
  <div class="wrap">
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
  </div>
</template>

<script>
//Conection with API

import axios from "axios";

export default {
  name: "SpotifyAPI",
  mounted() {
    this.fetchPlaylists(); // Call the function here
  },
  methods: {
    async fetchPlaylists() {
      try {
        // POST request
        const tokenResponse = await axios.post(
          "https://accounts.spotify.com/api/token",
          "grant_type=client_credentials&client_id=a6796a45306e48fcaa87626717314bfe&client_secret=2a63f4580d1649a98ad57ef7bfd78426",
          {
            headers: {
              "Content-Type": "application/x-www-form-urlencoded",
            },
          }
        );

        // Extract the access token from the response
        const token = tokenResponse.data.access_token;
        console.log(token);

        const headers = {
          Authorization: "Bearer " + { token },
        };

        const artistsUrl =
          "https://api.spotify.com/v1/artists/4Z8W4fKeB5YxbusRsdQVPb";

        const response = await axios.get(artistsUrl, { headers });

        if (response.status === 200) {
          const artistData = response.data;
          console.log("Artist information:", artistData);
        } else {
          console.error(
            "Error fetching artist information:",
            response.statusText
          );
        }
      } catch (error) {
        console.error("Error fetching playlists:", error);
      }
    },
  },
};
</script>

<style lang="scss" scoped>
.wrap {
  background-color: #302b27;
  width: 30%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 20px;
  margin: 30px 0;
  border-radius: 15px;
}
.song-card {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: space-between;
  color: black;
  width: 350px;
  border-radius: 5px;
  background-color: white;
  padding: 15px;
  margin: 15px;

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
