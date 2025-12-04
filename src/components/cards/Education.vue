<script>
export default {
  name: 'Education',
  props: {
    image: {
      type: String,
      required: true,
    },
    name: {
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
    percentage: {
      type: String,
      required: true,
    },
  },
}
</script>

<template>
  <div class="card education">
    <div class="education__header">
      <div class="education__emblem">
        <img :src="image" alt="" />
      </div>
      <div class="education__name">{{ name }}</div>
    </div>
    <div class="education__title">{{ title }}</div>
    <div class="education__subtitle">{{ subtitle }}</div>
    <div class="education__percentage">{{ percentage }}</div>
  </div>
</template>

<style scoped></style>
