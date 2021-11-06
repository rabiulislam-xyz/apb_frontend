<template>
  <nav class="flex items-center justify-between flex-wrap bg-green-500 p-6">
    <div class="flex items-center flex-shrink-0 text-white mr-6">
      <nuxt-link to="/">
        <a class="font-semibold text-xl tracking-tight"
          >Area Phonebook</a
        ></nuxt-link
      >
    </div>
    <div class="w-full block flex-grow lg:flex lg:items-center lg:w-auto">
      <div class="text-sm lg:flex-grow">
        <a
          v-if="$auth.loggedIn"
          href="#responsive-header"
          class="
            block
            mt-4
            lg:inline-block lg:mt-0
            text-teal-200
            hover:text-white
            mr-4
          "
        >
          Profile
        </a>
      </div>
      <div>
        <div
          href="#"
          class="
            block
            mt-4
            lg:inline-block lg:mt-0
            text-teal-200
            hover:text-white
            mr-4
          "
        >
          <a class="navbar-item" @click="logout" v-if="$auth.loggedIn" href="#"
            >Logout</a
          >
          <a class="navbar-item" v-else
            ><nuxt-link to="/login">Login</nuxt-link></a
          >
        </div>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  methods: {
    async logout() {
      await this.$auth.logout();
      this.$toast.show("Logged out");
      this.$router.push("login");
    },
  },
};
</script>
