<template>
  <div class="site-wrapper">
    <article class="site-contents">
      <nuxt />
    </article>
  </div>
</template>

<style lang="scss" scoped>
.site-wrapper {
  width: 100%;
  max-width: 414px;
  margin: 0 auto;
  background: $white;
  display: block;
  position: relative;
  overflow: hidden;
  min-height: 100vh;
  padding: 24px;
}

.site-contents {
  padding-top: 120px;
}
</style>
