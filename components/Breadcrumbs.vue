<template>
  <div>
    <v-breadcrumbs :items="items" divider="/"></v-breadcrumbs>
  </div>
</template>
<script>
export default {
  data: (instance) => ({
    items: [
      {
        text: "List",
        disabled: false,
        href: "/",
      },
      {
        text: instance.title,
        disabled: false,
        href: "#",
      },
    ],
  }),
  props: {
    title: {
      type: String,
      require: true,
    },
  },
  
};
</script>