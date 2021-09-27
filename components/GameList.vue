<template>
  <div>
    <v-container fluid>
      <v-row justify-content: start;>
        <v-col v-for="item in items" :key="item.id" cols="12" lg="4">
          <Card
            :id="item.id"
            :title="item.title"
            :thumbnail="item.thumbnail"
            :short_description="item.short_description"
          />
        </v-col>
      </v-row>
    </v-container>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  props: {
    items: {
      type: Array,
      require: true,
    },
  },
};
</script>
