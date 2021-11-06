<template>
  <section class="section">
    <div v-if="$auth.loggedIn">
      Hello! {{ $auth.user.email }} - {{ $auth.user }},
      <br />

      fill up this form below!
      <br />
      <button type="button" @click="logout">Logout</button>
    </div>
    <div v-else>
      You are not logged in,
      <a><nuxt-link to="/login">Click here to login</nuxt-link></a>
    </div>
  </section>
</template>

<script>
export default {
  // middleware: "auth",
  methods: {
    async logout() {
      console.log("logout");
      await this.$auth.logout();
      console.log("logout done");
      // this.$toast.show("Successfully logged out");
    },
  },
};
</script>
