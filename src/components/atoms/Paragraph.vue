<template>
  <p :class="`${type}`" class="paragraph"><slot></slot></p>
</template>

<script>
export default {
  props: {
    type: {
      type: String,
      default: "secondary",
    },
  },
};
</script>

<style scoped>
.paragraph {
  @apply text-sm py-2 pl-2;
}

.primary {
  @apply text-primary;
}

.secondary {
  @apply text-secondary;
}

.white {
  @apply text-white;
}
</style>
