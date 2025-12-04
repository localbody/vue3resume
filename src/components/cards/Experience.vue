<script>
export default {
  name: 'Experience',
  props: {
    date: {
      type: String,
      required: true,
    },
    location: {
      type: String,
      required: true,
    },
    image: {
      type: String,
      required: true,
    },

    role: {
      type: String,
      required: true,
    },
    name: {
      type: String,
      required: true,
    },
    description: {
      type: String,
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
            'experience__date--present': date.toLowerCase() == 'present',
          }"
        >
          {{ date }}
        </span>
        <div class="experience__location">{{ location }}</div>
      </div>
      <div class="experience__company">
        <div class="experience__company-logo">
          <img :src="image" alt="" />
        </div>
        <div class="experience__company-wrapper">
          <span class="experience__company-role">{{ role }}</span>
          <span class="experience__company-name">{{ name }}</span>
        </div>
      </div>
    </div>

    <p class="experience__description">{{ description }}</p>
  </div>
</template>

<style></style>
