<template>
  <div id="app" class="container mx-auto">
    <main-header />
    <newsletter :type="TYPE.PRIMARY" />
  </div>
</template>

<script>
import { TYPE } from "@/constants";
import MainHeader from "./components/organisms/MainHeader";
import Newsletter from "./components/organisms/Newsletter";

export default {
  name: "App",
  components: {
    MainHeader,
    Newsletter,
  },
  data() {
    return {
      TYPE,
    };
  },
};
</script>

<style></style>
