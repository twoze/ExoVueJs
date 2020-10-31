<template>
  <button class="btn-blue ">
    {{ text }}
  </button>
</template>

<script>
export default {
  props: ['text']
}
</script>

<style scoped>
.btn-blue {
  @apply bg-gray-200 py-2 px-4 rounded;}
.btn-blue:hover {
  @apply bg-orange-300;
}
</style>