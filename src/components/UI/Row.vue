<script>
export default {
  name: 'Row',
  props: {
    icon: {
      type: String,
      required: true,
    },
    title: {
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
  <div class="row">
    <div class="row__icon">
      <img :src="icon" alt="icon" />
    </div>
    <div class="row__wrapper">
      <span v-if="link != null" class="row__title">{{ title }}</span>
      <div class="row__subtitle">
        <!-- *normal? -->
        <template v-if="link == null">{{ title }}</template>
        <a v-else-if="link.href != null" class="row__link" :href="link.href">{{
          link.title
        }}</a>
        <span v-else class="row__text">{{ link.title }}</span>
      </div>
    </div>
  </div>
</template>

<style scoped></style>
