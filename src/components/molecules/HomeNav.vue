<template>
  <nav class="inline-block">
    <nav-menu>
      <link-item selected>Solutions</link-item>
      <link-item>Princing</link-item>
      <link-item :type="TYPE.PRIMARY">Docs</link-item>
      <link-item>More</link-item>
    </nav-menu>
  </nav>
</template>

<script>
import { TYPE } from "@/constants";

// ATOMS
import NavMenu from "@/components/atoms/NavMenu";
import LinkItem from "@/components/atoms/LinkItem";

export default {
  components: {
    NavMenu,
    LinkItem,
  },
  data() {
    return {
      TYPE,
    };
  },
};
</script>

<style></style>
