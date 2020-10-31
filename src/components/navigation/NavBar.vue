<template>
  <div class="hidden md:block md:ml-10 md:pr-4">
    <a href="#" class= "font-medium text-gray-500 hover:text-gray-900 transition duration-150 ease-in-out" @click="changeComponent('class-view')">Tous mes cours</a> |
    <a href="#" class= "font-medium text-gray-500 hover:text-gray-900 transition duration-150 ease-in-out" @click="changeComponent('selection-list')">Mes cours</a>
  </div>
</template>

<script>
export default {
  name: "nav-bar",
  methods: {
    changeComponent(value) {
      this.$emit('change-component', value)
    }
  }
}
</script>

<style>

</style>