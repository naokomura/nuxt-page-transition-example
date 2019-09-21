<template>
  <div class="navbar">
    <h1>{{ label }}</h1>
    <nav>
      <nuxt-link to="/">Home |</nuxt-link>
      <nuxt-link to="/one">Page One |</nuxt-link>
      <nuxt-link to="/two">Page Two</nuxt-link>
    </nav>
  </div>
</template>

<script>
export default {
  props: {
    label: {
      type: String,
      default: 'set this label prop'
    }
  }
}
</script>

<style lang="scss" scoped>
.navbar {
  position: fixed;
  top: 0;
  width: 100%;
  max-width: 414px;
  margin-left: -24px;
  background: $white;
  border-bottom: solid 1px;
  padding: 16px 24px;
}
</style>
