<template>
  <header class="flex items-center justify-between my-6">
    <logo />
    <home-nav />
    <sign />
  </header>
</template>

<script>
// ATOMS
import Logo from "../atoms/Logo.vue";

// MOLECULES
import HomeNav from "../molecules/HomeNav";
import Sign from "../molecules/Sign.vue";

export default {
  components: {
    Logo,
    HomeNav,
    Sign,
  },
};
</script>

<style></style>
