<template>
  <div class="text-center m-4 p-4 w-2/6 shadow-md">
    Panier : {{ selection.length }}
    <span v-if="numberSelection">cours</span>
    <span v-else>cours slectionnés</span>

    <ul>
      <li v-for="classSelec in selection" :key="classSelec.name">{{ classSelec.name }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "selection-box",
  props: ['selection'],
  computed: {
    numberSelection(){
      if(this.selection.length < 2){
        return true
      }
      return false
    }
  }
}
</script>

<style>

</style>