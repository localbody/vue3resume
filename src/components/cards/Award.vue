<script>
export default {
  name: 'Award',
  props: {
    image: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    subtitle: {
      type: String,
      required: true,
    },
    dates: {
      type: String,
      required: true,
    },
  },
}
</script>

<template>
  <div class="card award">
    <div class="award__logo">
      <img :src="image" alt="" />
    </div>

    <div class="award__wrapper">
      <span class="award__title">{{ title }}</span>
      <div class="award__subtitle">{{ subtitle }}</div>
    </div>
    <div class="award__dates">{{ dates }}</div>
  </div>
</template>

<style scoped></style>
