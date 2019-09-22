<template>
  <div>
    <NavBar label="HOME" />
    <main>
      <nav>
        <nuxt-link to="/level-2">Level 2 |</nuxt-link>
        <nuxt-link to="/test/layer-test">test</nuxt-link>
      </nav>
      <img src="~/assets/images/sample-1.jpg" alt />
      <h1>Lorem ipsum dolor sit amet, consectetur adipiscing elit</h1>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
      <h2>Lorem ipsum dolor sit amet, consectetur adipiscing elit</h2>
      <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
      <img src="~/assets/images/sample-2.jpg" alt />
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
      <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
      <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.</p>
      <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
    </main>
  </div>
</template>

<script>
import NavBar from "~/components/NavBar";

export default {
  transition: {
    name: "test",
    mode: ""
    // beforeEnter(el) {
    //   console.log("My transition");
    // }
  },
  components: {
    NavBar
  },
  data() {
    return {
      name
    };
  },
  asyncData({ from }) {
    console.log(from.path);
  }
};
</script>

<style>
nav {
  margin-bottom: 32px;
}
</style>
