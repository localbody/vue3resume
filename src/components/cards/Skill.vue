<script>
export default {
  name: 'Skill',
  props: {
    skill: {
      type: Object,
      required: true,
    },
  },
}
</script>

<template>
  <div class="card skill" :class="{ 'card--big': skill.isBigCard }">
    <div class="skill__logo">
      <img :src="skill.image" alt="" />
    </div>
    <div class="skill__title">{{ skill.title }}</div>
    <div class="skill__subtitle">{{ skill.subtitle }}</div>
  </div>
</template>

<style scoped></style>
