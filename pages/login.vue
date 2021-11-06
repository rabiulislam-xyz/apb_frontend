<template>
  <div>
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
        <i class="fa fa-google mr-2"></i>Login with Google
      </button>
    </div>
  </div>
</template>

<script>
export default {
  // middleware: "guest",
  methods: {
    loginWithGoogle() {
      this.$toast.show("Logging with google", { position: "top-right" });
      this.$auth.loginWith("google");
    },
  },
};
</script>
