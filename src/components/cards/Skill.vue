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

<style scoped>
.skill .skill__logo {
  width: 2rem;
  height: 2rem;
}

.skill.card--big .skill__logo {
  width: 3rem;
  height: 3rem;
}

.skill {
  display: grid;
  gap: 0.5rem;
  justify-items: center;
}

.skill__title {
  font-size: 0.875rem;
  font-weight: 500;
}

.skill__subtitle {
  font-size: 0.625rem;
  text-align: center;
  color: var(--gray-default);
}
</style>
