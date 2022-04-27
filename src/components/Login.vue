<template>
  <div class="container">
    <div class="form">
      <h1 class="text">Login</h1>

      <div class="login">
        <input type="text" v-model="email" placeholder="Enter Mail" />
        <input
          type="password"
          v-model="password"
          placeholder="Enter Password"
        />
        <div class="btn-container">
          <button class="button" v-on:click="login">Login</button>
        <p>
          <router-link to="/sign-up" class="link-style">Sign-Up</router-link>
        </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "Login",
  data() {
    return {
      email: "",
      password: "",
    };
  },
  methods: {
    async login() {
      let result = await axios.get(
        `http://localhost:3000/users?email=${this.email}&password=${this.password}`
      );
      if (result.status == 200 && result.data.length > 0) {
        localStorage.setItem("user-info", JSON.stringify(result.data[0]));
        this.$router.push({ name: "Home" });
      }
      console.warn(result);
    },
  },
  mounted() {
    let user = localStorage.getItem("user-info");
    if (user) {
      this.$router.push({ name: "Home" });
    }
  },
};
</script>
