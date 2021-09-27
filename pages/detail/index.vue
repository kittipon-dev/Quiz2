<template></template>
<script>
export default {
  asyncData(context) {
    if (!context.route.params.detail) {
      context.redirect("/");
    }
  },
};
</script>