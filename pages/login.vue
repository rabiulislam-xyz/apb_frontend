<template>
  <div>
    <nuxt-link to="/">
      <button class="text-black bg-white hover:bg-gray-100">Back</button>
    </nuxt-link>
    <div
      class="
        pt-4
        bg-white
        w-full
        md:w-56
        justify-center
        items-center
        shadow
        px-6
        py-4
        flex flex-col
      "
    >
      Login with

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
