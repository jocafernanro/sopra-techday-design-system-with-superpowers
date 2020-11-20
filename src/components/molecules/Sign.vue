<template>
  <div class="flex inline-block">
    <Button text="Sign in"></Button>
    <Button text="Sign up" :type="TYPE.PRIMARY"></Button>
  </div>
</template>

<script>
import { TYPE } from "@/constants";
import Button from "@/components/atoms/Button.vue";

export default {
  components: {
    Button,
  },
  data() {
    return {
      TYPE,
    };
  },
};
</script>

<style></style>
