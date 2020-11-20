<template>
  <component :is="level" :class="[`${level}`, `${type}`]" class="title"
    ><slot></slot
  ></component>
</template>

<script>
export default {
  props: {
    level: {
      type: String,
      required: true,
      validator: function(value) {
        console.log(value);
        return value.match("h[1-6]");
      },
    },
    type: {
      type: String,
      default: "secondary",
    },
  },
};
</script>

<style scoped>
.title {
  font-family: "Manrope";
  @apply inline-block tracking-tight font-bold;
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

.h1 {
  @apply text-6xl;
}

.h2 {
  @apply text-5xl;
}

.h3 {
  @apply text-4xl;
}

.h4 {
  @apply text-3xl;
}

.h5 {
  @apply text-2xl font-medium;
}

.h6 {
  @apply text-xl font-medium;
}
</style>
