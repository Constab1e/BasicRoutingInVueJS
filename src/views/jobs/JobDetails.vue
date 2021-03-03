<template>
  <h1>Job Details Page</h1>
  <p>Job id is {{ id }}</p>
  <p>Job title is {{ title }}</p>
  <p>Job details is {{ details }}</p>
</template>

<script>
export default {
  props: ["id", "title", "details"],
  //   data() {
  //     return {
  //       id: this.$route.params.id,
  //       title: this.$route.params.title,
  //       details: this.$route.params.details,
  //     };
  //   },
};
</script>

<style>
</style>