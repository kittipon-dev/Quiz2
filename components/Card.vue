<template>
  <v-card :to="'/detail/'+id">
    <v-container id="card">
      <v-row>
        <v-col cols="6" md="12" sm="12" lg="12">
          <v-img :src="thumbnail" class="image"></v-img>
        </v-col>
        <v-col cols="6" md="12" sm="12" lg="12">
          <strong id="title">{{ title }}</strong>
          <div id="short_description">
            {{ short_description }}
          </div>
        </v-col>
      </v-row>
    </v-container>
  </v-card>
</template>
<style scoped>
.image {
  border-radius: 8px;
}
#card {
  background-color: white;
  min-height: 290px;
}
@media screen and (max-device-width: 600px) {
  #card {
    background-color: white;
    min-height: 90px;
  }
  .image {
    border-radius: 8px;
    height: 90px;
  }
}
</style>

<script>
export default {
  methods: {
    select: function (url) {
      window.location.href = url;
    },
  },
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