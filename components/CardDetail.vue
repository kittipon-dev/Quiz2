<template>
  <v-container id="card">
    <v-row>
      <v-col cols="12" lg="12">
        <v-img :src="thumbnail" id="image"></v-img>
      </v-col>
      <v-col cols="12" lg="12">
        <div id="detail">
          <strong id="title">{{ title }}</strong>
          <br />
          <br />
          <div id="short_description">
            {{ short_description }}
          </div>
        </div>
      </v-col>
    </v-row>
  </v-container>
</template>

<style scoped>
#image {
  border-radius: 8px;
  width: 100%;
}
#card {
  background-color: white;
  padding: 10px;
  max-width: 920px;
}
@media screen and (max-device-width: 600px) {
  #card {
    background-color: #e5e5e5;
  }
  #detail {
    border-radius: 8px;
    background-color: #ffffff;
    padding: 1rem;
  }
}
</style>

<script>
export default {
  props: {
    id: {
      type: Number,
      require: true,
    },
    thumbnail: {
      type: String,
      require: true,
    },
    title: {
      type: String,
      require: true,
    },
    short_description: {
      type: String,
      require: true,
    },
  },
};
</script>