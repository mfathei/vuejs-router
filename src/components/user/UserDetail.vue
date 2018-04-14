<template>
    <div>
        <h3>Some User Details</h3>
        <p>User loaded id : {{ $route.params.id }}</p>
        <router-link tag="button" 
        :to="link"
        class="btn btn-primary">Edit User</router-link>
    </div>
</template>

<script>
export default {
  data() {
    return {
      link: {
        name: "editUser",
        params: { id: this.$route.params.id },
        query: { locale: "en", q: 100 },
        hash: "#data"
      }
    };
  },
  beforeRouteEnter(to, from, next) {
    if (true) {
      next();
    } else {
      console.log("You don't have permissions to view user details");
      next(false);
    }
  }
};
</script>
