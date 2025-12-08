<script>
import Aside from '@/components/layout/Aside.vue'
import Main from '@/components/layout/Main.vue'

export default {
  name: 'App',
  components: {
    Aside,
    Main,
  },
}
</script>

<template>
  <div class="container">
    <Aside />
    <Main />
  </div>
</template>

<style scoped>
.container {
  display: grid;
  grid-template-columns: 1fr 1fr;
  width: min-content;
  margin: 0 auto;
}

@media (max-width: 1200px) {
  .container {
    grid-template-columns: 1fr;
  }
}
</style>
