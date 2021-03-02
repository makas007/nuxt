<template>
  <section>
    <h1>Login page</h1>
    <form @submit.prevent="onSubmit">
      <div>
        <input type="text" class="form-control" />
      </div>
      <p>
        <nuxt-link to="/">To home page</nuxt-link>
      </p>
      <button class="btn btn-primary" type="submit">Login</button>
    </form>
  </section>
</template>

<script>
export default {
  methods: {
    onSubmit() {
      this.$store.dispatch("login")
      this.$router.push("/")
    },
  },
}
</script>
