<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    {{ this.$store.state.user.user }}
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
  created() {
    this.$store.dispatch("user/saveUser", { name: "running" });
  },
};
</script>
