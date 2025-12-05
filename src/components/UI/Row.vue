<script>
export default {
  name: 'Row',
  props: {
    row: {
      type: Object,
      required: true,
    },
  },
}
</script>
<template>
  <div class="row">
    <div class="row__icon">
      <img :src="row.icon" alt="icon" />
    </div>
    <div class="row__wrapper">
      <span v-if="link != null" class="row__title">{{ row.title }}</span>
      <div class="row__subtitle">
        <!-- *normal? -->
        <template v-if="row.link == null">{{ row.title }}</template>
        <a
          v-else-if="row.link.href != null"
          class="row__link"
          :href="row.link.href"
          >{{ row.link.title }}</a
        >
        <span v-else class="row__text">{{ row.link.title }}</span>
      </div>
    </div>
  </div>
</template>

<style scoped>
.row {
  display: grid;
  grid-template-columns: 2rem 1fr;
  gap: 1rem;
  align-items: center;
}

.row__wrapper {
  display: grid;
  gap: 0.5rem;
}

.rows--infos .row__icon {
  width: 2rem;
  height: 2rem;
  border-radius: 100%;
  background-color: var(--gray-lightest);
  display: grid;
  place-content: center;
}

.rows--infos .row__icon img {
  width: 16px;
  height: 16px;
}

.row__title {
  font-size: 0.75rem;
  color: var(--gray-default);
}

.row__text,
.row__link {
  font-size: 0.875rem;
  font-weight: 500;
  color: var(--gray-dark);
  text-decoration: none;
}

.row__link--underline {
  text-decoration: underline;
}

@media (max-width: 440px) {
  .row__subtitle {
    overflow: hidden;
    text-overflow: ellipsis;
    line-height: 125%;
  }
}
</style>
