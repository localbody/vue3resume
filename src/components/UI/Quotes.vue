<script>
export default {
  name: 'Quotes',
  props: {
    text: {
      type: String,
      required: true,
    },
  },
}
</script>

<template>
  <div class="quotes">{{ text }}</div>
</template>

<style scoped>
.quotes {
  font-size: 1.125rem;
  color: var(--gray-dark);
  font-weight: 500;
  line-height: 1.5rem;
  letter-spacing: 0.02rem;
}
</style>
