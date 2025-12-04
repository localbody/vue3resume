<script>
export default {
  name: 'Skill',
  props: {
    isBigCard: {
      type: Boolean,
      required: true,
    },
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
  },
}
</script>

<template>
  <div class="card skill" :class="{ 'card--big': isBigCard }">
    <div class="skill__logo">
      <img :src="image" alt="" />
    </div>
    <div class="skill__title">{{ title }}</div>
    <div class="skill__subtitle">{{ subtitle }}</div>
  </div>
</template>

<style scoped></style>
