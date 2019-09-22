<template>
  <header class="navbar">
    <nav v-if="isChild" @click="routerBack">
      <svg width="24" height="24" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg">
        <path
          d="M15.0176 20.2793C15.2324 20.4941 15.5059 20.6113 15.8281 20.6113C16.4727 20.6113 16.9902 20.1035 16.9902 19.459C16.9902 19.1367 16.8535 18.8438 16.6289 18.6191L9.79297 11.9395L16.6289 5.2793C16.8535 5.05469 16.9902 4.75195 16.9902 4.43945C16.9902 3.79492 16.4727 3.28711 15.8281 3.28711C15.5059 3.28711 15.2324 3.4043 15.0176 3.61914L7.41992 11.041C7.14648 11.2949 7.01953 11.6074 7.00977 11.9492C7.00977 12.291 7.14648 12.584 7.41992 12.8477L15.0176 20.2793Z"
        />
      </svg>
      <p>Back</p>
    </nav>
    <h1>{{ label }}</h1>
  </header>
</template>

<script>
export default {
  props: {
    label: {
      type: String,
      default: "set this label prop"
    },
    isChild: {
      type: Boolean,
      default: false
    }
  },

  methods: {
    routerBack() {
      if (this.backType === "logo") {
        this.$router.push("/");
      } else {
        this.$router.back();
      }
    }
  }
};
</script>

<style lang="scss" scoped>
.navbar {
  position: fixed;
  top: 0;
  width: 100%;
  max-width: 414px;
  margin-left: -24px;
  background: rgba($gray-1, 0.92);
  border-bottom: solid 1px $bd-black;
  padding: 12px 16px;
  z-index: 9;
  text-align: center;
  backdrop-filter: blur(24px);

  > nav {
    display: flex;
    align-items: center;
    position: absolute;
    top: 50%;
    left: 8px;
    transform: translateY(-50%);
    color: $primary;
    cursor: pointer;

    > svg {
      margin-right: 4px;
      fill: $primary;
    }

    > p {
      @include body;
    }
  }

  > h1 {
    margin-bottom: 0;
    @include strong;
  }
}
</style>
