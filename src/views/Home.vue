<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <div>Username: {{ user.username }} Email: {{ user.email }}</div>
    <HelloWorld msg="Welcome to Your Vue.js App" />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";

export default {
  name: "Home",
  components: {
    HelloWorld,
  },
  computed: {
    user() {
      return this.$store.state.authUser;
    },
  },
};
</script>
