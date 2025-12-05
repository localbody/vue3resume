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

<style scoped></style>
