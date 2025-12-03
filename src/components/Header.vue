<script>
export default {
  name: 'Header',
  props: {
    src: {
      type: String,
      required: true
    },
    alt: {
      type: String,
      default: ''
    },
    name: {
      type: String,
      required: true
    }
  }
};
</script>

<template>
  <div class="header">
    <div class="header__photo">
      <img :src="src" :alt="alt" />
    </div>
    <h1 class="header__name">{{ name }}</h1>
  </div>
</template>

<style scoped>

</style>
