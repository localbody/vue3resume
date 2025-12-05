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

<style scoped>
.project {
  display: grid;
  grid-template-areas:
    'project__logo project__name'
    'project__logo project__description'
    'project__footer project__footer';
  column-gap: 1rem;
  row-gap: 0.5rem;
}

.project__logo {
  grid-area: project__logo;
  width: 3rem;
  height: 3rem;
}

.project__name {
  grid-area: project__name;
  font-size: 1rem;
  font-weight: 500;
  color: var(--gray-darker);
}

.project__description {
  grid-area: project__description;
  font-size: 0.875rem;
  font-weight: 300;
  color: var(--gray-default);
}

.project__footer {
  grid-area: project__footer;
  display: flex;
  gap: 0.75rem;
  align-items: center;
}

.project__footer-logo {
  width: 1.5rem;
  height: 1.5rem;
  border-radius: 100%;
  background-color: var(--secondary--lighter);
  padding: 0.375rem;
  display: grid;
  place-content: center;
  flex-shrink: 0;
}

.project__link {
  font-size: 1rem;
  font-weight: 500;
  color: var(--secondary--default);
}

@media (max-width: 900px) {
  .project {
    width: 100%;
    justify-content: flex-start;
  }
}

@media (max-width: 440px) {
  .project__link-wrapper {
    overflow: hidden;
    text-overflow: ellipsis;
    line-height: 125%;
  }

  .project__link-wrapper {
    max-width: calc(100vw - 12rem);
  }
}
</style>
