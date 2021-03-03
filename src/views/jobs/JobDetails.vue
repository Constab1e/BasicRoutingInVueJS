<template>
  <div v-if="job">
    <h1>Job Details Page</h1>
    <h1>Job title is {{ job.title }}</h1>
    <p>Job id is {{ job.id }}</p>
    <h3>{{ job.details }}</h3>
  </div>
</template>

<script>
export default {
  props: ["id", "title", "details"],
  data() {
    return {
      job: null,
    };
  },
  mounted() {
    fetch("http://localhost:3000/jobs/" + this.id)
      .then((res) => res.json())
      .then((data) => (this.job = data))
      .catch((err) => console.log(err.message));
  },
};
</script>

<style>
</style>