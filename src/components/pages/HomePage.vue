<template>
  <single-page>
    <template slot="header">
      <main-header />
    </template>

    <template slot="newsletter">
      <newsletter :type="TYPE.PRIMARY" />
    </template>
  </single-page>
</template>

<script>
import { TYPE } from "@/constants";

// ORGANISMS
import MainHeader from "../organisms/MainHeader";
import Newsletter from "../organisms/Newsletter";

// TEMPLATE
import SinglePage from "../templates/SinglePage";

export default {
  components: {
    MainHeader,
    Newsletter,
    SinglePage,
  },

  data() {
    return {
      TYPE,
    };
  },
};
</script>

<style></style>
