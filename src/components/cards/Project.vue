<script>
export default {
  name: 'Project',
  props: {
    image: {
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
    logo: {
      type: String,
      required: true,
    },
    link: {
      type: Object,
      required: true,
    },
  },
}
</script>

<template>
  <div class="card project">
    <div class="project__logo">
      <img :src="image" alt="" />
    </div>
    <h3 class="project__name">{{ name }}</h3>
    <p class="project__description">
      {{ description }}
    </p>
    <div class="project__footer">
      <div class="project__footer-logo">
        <img :src="logo" alt="" />
      </div>
      <a class="project__link" :href="link.url">{{ link.anchor }}</a>
    </div>
  </div>
</template>

<style></style>
