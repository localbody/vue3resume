<script>
export default {
  name: 'Education',
  props: {
    education: {
      type: Object,
      required: true,
    },
  },
}
</script>

<template>
  <div class="card education">
    <div class="education__header">
      <div class="education__emblem">
        <img :src="education.image" alt="" />
      </div>
      <div class="education__name">{{ education.name }}</div>
    </div>
    <div class="education__title">{{ education.title }}</div>
    <div class="education__subtitle">{{ education.subtitle }}</div>
    <div class="education__percentage">{{ education.percentage }}</div>
  </div>
</template>

<style scoped></style>
