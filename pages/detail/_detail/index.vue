<template>
  <v-container style="max-width:920px;">
    <Breadcrumbs :title="data.title" />
    <CardDetail
      :thumbnail="data.thumbnail"
      :title="data.title"
      :short_description="data.short_description"
    />
  </v-container>
</template>

<script>
import axios from "axios";
export default {
  data() {
    return { data: {} };
  },
  asyncData(context) {
    return axios
      .get("https://free-to-play-games-database.p.rapidapi.com/api/game", {
        headers: {
          "x-rapidapi-key":
            "2a50aee9e6msh55cf8498c0e6c1ap1c932fjsn9403eb2b255d",
          "x-rapidapi-host": "free-to-play-games-database.p.rapidapi.com",
        },
        params: { id: context.route.params.detail },
      })
      .then((res) => {
        return { data: res.data };
      })
      .catch(function (error) {
        context.redirect("/");
      });
  },
};
</script>
