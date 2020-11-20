<template>
  <input class="input" :type="type" name="input" :placeholder="placeholder" />
</template>

<script>
export default {
  props: {
    placeholder: {
      type: String,
      required: true,
    },
    type: {
      type: String,
      requierd: true,
    },
  },
};
</script>

<style scoped>
.input {
  @apply bg-gray-100 px-6 py-3 mr-4 font-semibold rounded-lg;
}
</style>
