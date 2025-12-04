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

<style scoped></style>
