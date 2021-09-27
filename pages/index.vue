<template>
  <div>
    <Header />
    <v-container>
      <GameList :items="list" />
    </v-container>
  </div>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return { list: [] };
  },
  asyncData(context) {
    return axios
      .get("https://free-to-play-games-database.p.rapidapi.com/api/games", {
        headers: {
          "x-rapidapi-key":
            "2a50aee9e6msh55cf8498c0e6c1ap1c932fjsn9403eb2b255d",
          "x-rapidapi-host": "free-to-play-games-database.p.rapidapi.com",
        },
      })
      .then((res) => {
        return { list: res.data };
      });
  },
};
</script>
