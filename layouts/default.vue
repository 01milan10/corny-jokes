<template>
  <div class="antialiased">
    <headNav />
    <Nuxt />
  </div>
</template>

<script>
import headNav from "./headNav";
export default {
  components: {
    headNav,
  },
};
</script>

<style>
html,
body {
  margin: 0;
  padding: 0;
  @apply bg-gray-300;
}
</style>