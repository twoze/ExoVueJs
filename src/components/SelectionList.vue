<template>
  <h1>Mes Cours</h1>

  <div v-if="selection.length == 0">
    <p>Aucun cours sélectionné</p>
  </div>

  <div v-else>
    <div
      v-for="classSelec in selection"
      :key="classSelec.name" 
      class="border border-black my-4 p-2"
    >
      <h3>{{ classSelec.name }} ({{ classSelec.number }})</h3>

    </div>
  </div>
</template>



<script>
export default {
  name: "selection-list",
  props: ['selection']
}
</script>

<style>
</style>