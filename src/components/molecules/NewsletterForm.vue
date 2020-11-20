<template>
  <form @submit.prevent class="grid grid-cols-6 my-3">
    <Input class="col-span-4 self-start" />
    <Button class="col-span-2 " :type="buttonType" :text="'Notify me'" />
    <Paragraph class="col-span-6" :type="paragraphType"
      >We care about the protection of your data. Read our
      <a class="underline">Privacy Policy</a></Paragraph
    >
  </form>
</template>

<script>
import { TYPE } from "@/constants";
import Input from "../atoms/Input";
import Button from "../atoms/Button";
import Paragraph from "../atoms/Paragraph";
export default {
  props: {
    type: {
      type: String,
      default: "primary",
    },
  },
  components: {
    Input,
    Button,
    Paragraph,
  },
  data() {
    return {
      TYPE,
    };
  },
  computed: {
    buttonType() {
      let buttonType;

      switch (this.type) {
        case TYPE.PRIMARY:
        case TYPE.DEFAULT:
          buttonType = TYPE.SECONDARY;
          break;
        case TYPE.SECONDARY:
          buttonType = TYPE.PRIMARY;
          break;
      }

      console.log(buttonType);

      return buttonType;
    },
    paragraphType() {
      let paragraphType = TYPE.SECONDARY;
      if ([TYPE.PRIMARY, TYPE.SECONDARY].includes(this.type))
        paragraphType = TYPE.WHITE;
      return paragraphType;
    },
  },
};
</script>

<style></style>
