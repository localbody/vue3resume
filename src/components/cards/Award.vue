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

<style scoped>
.award {
  display: flex;
  gap: 1rem;
}

.award__logo {
  width: 2.625rem;
  height: 2.625rem;
}

.award__wrapper {
  justify-self: flex-start;
  display: grid;
  gap: 0.25rem;
}

.award__title {
  font-size: 0.875rem;
  color: var(--gray-default);
  font-weight: 300;
}

.award__subtitle {
  font-size: 1rem;
  color: var(--gray-darker);
  font-weight: 500;
}

.award__dates {
  flex-grow: 2;
  text-align: right;
  color: var(--gray-dark);
  font-size: 0.75rem;
  font-weight: 300;
}
</style>
