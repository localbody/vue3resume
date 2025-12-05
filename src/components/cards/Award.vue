<script>
export default {
  name: 'Award',
  props: {
    award: {
      type: Object,
      required: true,
    },
  },
}
</script>

<template>
  <div class="card award">
    <div class="award__logo">
      <img :src="award.image" alt="" />
    </div>

    <div class="award__wrapper">
      <span class="award__title">{{ award.title }}</span>
      <div class="award__subtitle">{{ award.subtitle }}</div>
    </div>
    <div class="award__dates">{{ award.dates }}</div>
  </div>
</template>

<style scoped></style>
