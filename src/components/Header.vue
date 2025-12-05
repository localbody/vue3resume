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

<style scoped>
.header {
  display: grid;
  gap: 1rem;
}

.header__photo {
  width: 6rem;
  height: 6rem;
  border-radius: 100%;
  overflow: hidden;
}

.header__name {
  font-weight: 500;
  font-size: 2rem;
  line-height: 2.5rem;
  color: var(--gray-darker);
}
</style>
