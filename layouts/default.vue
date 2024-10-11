<template>
  <v-app>
    <Nuxt />
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout'
}
</script>

<style>
.page-enter-active, .page-leave-active {
  transition: transform 0.5s ease-in-out;
}

.page-enter {
  transform: translateY(100%);
}

.page-leave-to {
  transform: translateY(-100%);
}
</style>
