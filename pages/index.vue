<template>
  <section class="section">
    Hello! {{ $auth.user.email }},
    <br />
    fill up this form below!
    <br />
    <nuxt-link to="/logout">Logout</nuxt-link>
  </section>
</template>

<script>
export default {
  middleware: "auth",
};
</script>
