<script>
export default {
  name: 'Project',
  props: {
    project: {
      type: Object,
      required: true,
    },
  },
}
</script>

<template>
  <div class="card project">
    <div class="project__logo">
      <img :src="project.image" alt="" />
    </div>
    <h3 class="project__name">{{ project.name }}</h3>
    <p class="project__description">
      {{ project.description }}
    </p>
    <div class="project__footer">
      <div class="project__footer-logo">
        <img :src="project.logo" alt="" />
      </div>
      <div class="project__link-wrapper">
        <a class="project__link" :href="project.link.url">{{
          project.link.anchor
        }}</a>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
