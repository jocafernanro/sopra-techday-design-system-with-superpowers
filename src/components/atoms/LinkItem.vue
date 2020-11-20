<template>
  <li :class="[`${color}`]" class="link-item hover:text-primary">
    <a class="no-underline" href="#">
      <slot></slot>
    </a>
  </li>
</template>

<script>
import { TYPE } from "@/constants";

export default {
  props: {
    type: {
      type: String,
      default: "default",
    },
    selected: {
      type: Boolean,
      default: false,
    },
  },

  computed: {
    color() {
      return this.selected ? TYPE.SELECTED : this.type;
    },
  },
};
</script>

<style scoped>
.link-item {
  @apply text-lg font-semibold mr-6;
}

.default {
  @apply text-gray-400;
}

.selected {
  @apply text-black;
}

.primary {
  @apply text-primary;
}

.secondary {
  @apply text-secondary;
}
</style>
