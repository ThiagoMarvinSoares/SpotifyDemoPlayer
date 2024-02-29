<template>
</template>

<script>
import axios from 'axios';

export default {
  name: 'SpotifyAPI',
  async fetchPlaylists() {
    try {
      // POST request
      const tokenResponse = await axios.post(
        'https://accounts.spotify.com/api/token',
        'grant_type=client_credentials&client_id=a6796a45306e48fcaa87626717314bfe&client_secret=2a63f4580d1649a98ad57ef7bfd78426',
        {
          headers: {
            'Content-Type': 'application/x-www-form-urlencoded'
          }
        }
      );
      
      // Extract the access token from the response
      const token = tokenResponse.data.access_token;

      console.log(token);
      
    } catch (error) {
      console.error('Error fetching playlists:', error);
    }
  }
};
</script>