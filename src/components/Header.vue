<template>
  <div class="nav">
    <router-link to="/">Home</router-link>
    <router-link to="/add">Add</router-link>
    <router-link to="update">Update</router-link>
    <a v-on:click="logout" href="#">Logout</a>
  </div>
</template>
<script>
export default {
  name: "Header",
  methods: {
    logout() {
      localStorage.clear();
      this.$router.push({ name: "Login" });
    },
  },
};
</script>
<style>
.nav {
  background-color: black;
  overflow: hidden;
  display: flex;
  justify-content: center;
  /* position: fixed; */
}
.heading {
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
}

.nav a {
  float: left;
  color: rgb(241, 240, 255);
  padding: 14px 16px;
  text-align: center;
  font-size: 17px;
  text-decoration: none;
  margin-right: 5px;
}
.nav a:hover {
  /* background: #fff0f5; */
  color: rgb(214, 189, 189);
}
</style>