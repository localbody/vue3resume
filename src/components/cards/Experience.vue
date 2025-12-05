<script>
export default {
  name: 'Experience',
  props: {
    experience: {
      type: Object,
      required: true,
    },
  },
}
</script>

<template>
  <div class="experience">
    <div class="experience__wrapper">
      <div class="experience__inner">
        <span
          class="experience__date"
          :class="{
            'experience__date--present':
              experience.date.toLowerCase() == 'present',
          }"
        >
          {{ experience.date }}
        </span>
        <div class="experience__location">{{ experience.location }}</div>
      </div>
      <div class="experience__company">
        <div class="experience__company-logo">
          <img :src="experience.image" alt="" />
        </div>
        <div class="experience__company-wrapper">
          <span class="experience__company-role">{{ experience.role }}</span>
          <span class="experience__company-name">{{ experience.name }}</span>
        </div>
      </div>
    </div>

    <p class="experience__description">{{ experience.description }}</p>
  </div>
</template>

<style scoped>
.experience {
  position: relative;
  display: flex;
}

.experience::before {
  content: '';
  position: absolute;
  left: -2.5rem;
  top: 0;
  display: block;
  width: 1.5rem;
  height: 1.5rem;
  border-radius: 100%;
  background-color: white;
}

.experience::after {
  content: '';
  position: absolute;
  left: -2rem;
  top: 0.5rem;
  display: flex;
  width: 0.375rem;
  height: 0.375rem;
  border-radius: 100%;
  background-color: var(--gray-darker);
}

.experience__wrapper {
  display: grid;
  gap: 1rem;
  width: 15.125rem;
  flex-shrink: 0;
}

.experience__inner {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}
.experience__date {
  font-size: 0.625rem;
  color: var(--gray-dark);
}

.experience__date--present {
  color: var(--primary-default);
  background-color: #efe2f9;
  border-radius: 0.25rem;
  padding: 0.005rem 0.5rem;
}

.experience__location {
  font-size: 0.625rem;
  color: var(--gray-default);
  display: flex;
  gap: 0.25rem;
  align-items: center;
}

.experience__location::before {
  content: '';
  width: 0.75rem;
  height: 0.75rem;
  background-image: url(../icons/location.svg);
  background-position: center;
  background-repeat: no-repeat;
  background-size: contain;
  flex-shrink: 0;
}

.experience__company {
  display: flex;
  gap: 1rem;
}

.experience__company-wrapper {
  display: grid;
}

.experience__company-logo {
  width: 2.5rem;
  height: 2.5rem;
}

.experience__company-role {
  color: var(--gray-default);
  font-size: 0.75rem;
}

.experience__company-name {
  font-size: 0.875rem;
  color: var(--gray-darker);
}

.experience__description {
  font-size: 0.75rem;
  color: var(--gray-default);
  line-height: 1.5rem;
}

@media (max-width: 900px) {
  .experience {
    display: grid;
  }
}
</style>
