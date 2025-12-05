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

<style scoped>
.cards--education > .card {
  flex-grow: 1;
  flex-basis: 0;
}

.education {
  display: grid;
  align-items: center;
  gap: 0.25rem;
}

.education__header {
  display: flex;
  gap: 1rem;
  align-items: center;
}

.education__emblem {
  width: 2.375rem;
  height: 3rem;
}

.education__name {
  font-size: 0.75rem;
  color: var(--gray-darker);
  font-weight: 600;
}

.education__title {
  font-size: 0.875rem;
  color: var(--gray-darker);
  font-weight: 500;
}

.education__subtitle {
  font-size: 0.625rem;
  color: var(--gray-default);
}

.education__percentage {
  font-size: 0.75rem;
  color: var(--gray-default);
  display: flex;
  gap: 0.25rem;
}

.education__percentage::before {
  content: 'Percentage';
  color: var(--iris);
}
</style>
