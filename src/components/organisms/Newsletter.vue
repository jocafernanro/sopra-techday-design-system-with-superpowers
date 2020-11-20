<template>
  <section :class="[`${type}`]" class="newsletter">
    <newsletter-titles :titleType="titleType" />
    <newsletter-form :type="type" />
  </section>
</template>

<script>
import { TYPE } from "@/constants";
import NewsletterTitles from "../molecules/NewsletterTitles";
import NewsletterForm from "../molecules/NewsletterForm";

export default {
  props: {
    type: {
      type: String,
      default: "default",
    },
  },
  components: {
    NewsletterTitles,
    NewsletterForm,
  },
  computed: {
    titleType() {
      let titleType = TYPE.SECONDARY;
      if ([TYPE.PRIMARY, TYPE.SECONDARY].includes(this.type))
        titleType = TYPE.WHITE;
      return titleType;
    },
  },
};
</script>

<style scoped>
.newsletter {
  @apply flex flex-col lg:flex-row lg:items-center justify-between px-14 py-10 rounded-lg;
}

.primary {
  @apply bg-primary;
}

.secondary {
  @apply bg-secondary;
}

.default {
  @apply bg-gray-50;
}
</style>
