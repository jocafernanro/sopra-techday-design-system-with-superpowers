<template>
  <div class="flex flex-col justify-between">
    <Title :level="TITLE.H3" :type="titleType">
      Want products news and updates?</Title
    >
    <Title :level="TITLE.H5" :type="titleType"
      >Sign up for our newsletter to stay up to date.</Title
    >
  </div>
</template>

<script>
import { TITLE } from "@/constants";
import Title from "../atoms/Title";

export default {
  props: {
    titleType: {
      type: String,
      default: "secondary",
    },
  },
  components: {
    Title,
  },
  data() {
    return {
      TITLE,
    };
  },
};
</script>

<style scoped></style>
