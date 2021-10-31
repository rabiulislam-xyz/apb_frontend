<template>
  <section class="section">
      Hello! {{ $auth.user.email }},
      <br>
      fill up this form below! 
  </section>
</template>

<script>
export default {
  middleware: 'auth'
};
</script>
