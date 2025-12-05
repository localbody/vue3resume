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

<style scoped></style>
