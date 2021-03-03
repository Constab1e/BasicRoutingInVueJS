<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link :to="{ name: 'About' }">About</router-link> |
    <router-link :to="{ name: 'Jobs' }">Jobs</router-link>
  </div>
  <button @click="back">Go Back</button>
  <button @click="forward">Go Forward</button>

  <router-view />
</template>

<script>
export default {
  methods: {
    forward() {
      this.$router.go(1);
    },
    back() {
      this.$router.go(-1);
    },
  },
};
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
  text-decoration: none;
  padding: 10px;
  border-radius: 4px;
}

#nav a.router-link-exact-active {
  color: white;
  background: green;
}
button {
  border-radius: 5px;
  padding: 10px;
  color: #2c3e50;
  margin: 0 5px;
  border: none;
}
</style>
