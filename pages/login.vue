<template>
  <!-- <section class="section">
    <b-button @click="loginWithGoogle()" icon-left="google">
      Sign in with Google
    </b-button>
  </section> -->
  <div>
    <button
      class="
        uppercase
        h-12
        mt-3
        text-white
        w-full
        rounded
        bg-blue-800
        hover:bg-blue-900
      "
    >
      <i class="fa fa-facebook mr-2"></i>Facebook
    </button>
    <button
      @click="loginWithGoogle()"
      class="
        uppercase
        h-12
        mt-3
        text-white
        w-full
        rounded
        bg-red-800
        hover:bg-red-900
      "
    >
      <i class="fa fa-google mr-2"></i>Google
    </button>
  </div>
</template>

<script>
export default {
  methods: {
    loginWithGoogle() {
      this.$auth.loginWith("google");
    },
  },
};
</script>
