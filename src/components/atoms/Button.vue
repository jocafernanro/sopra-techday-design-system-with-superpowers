<template>
  <button :class="[`${type}`]" class="button">{{ text }}</button>
</template>

<script>
export default {
  props: {
    type: {
      type: String,
      default: "default",
    },
    text: {
      type: String,
      required: true,
    },
  },
};
</script>

<style scoped>
.button {
  font-family: "Manrope";
  @apply text-lg font-semibold  px-8 py-2  rounded-lg;
}

.primary {
  @apply text-white bg-primary shadow-sm;
}

.secondary {
  @apply text-white bg-secondary shadow-sm;
}
</style>
