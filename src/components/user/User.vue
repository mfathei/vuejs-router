<template>
    <div>
        <h1>The User Page</h1>
        <hr>
        <p>Loaded id: {{ id }}</p>
        <button class="btn btn-primary" @click="navigateToHome">Go To Home</button>
    </div>
</template>

<script>
export default {
  data() {
    return {
      id: this.$route.params.id
    };
  },
  methods: {
    navigateToHome() {
      this.$router.push("/");
    }
  }
};
</script>
