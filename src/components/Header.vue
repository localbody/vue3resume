<script>
export default {
  name: 'Header',
  props: {
    photo: {
      type: String,
      required: true,
    },
    name: {
      type: String,
      required: true,
    },
  },
}
</script>

<template>
  <div class="header">
    <div class="header__photo">
      <img :src="photo" :alt="name" />
    </div>
    <h1 class="header__name">{{ name }}</h1>
  </div>
</template>

<style scoped></style>
