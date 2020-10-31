<template>

  <nav-bar
    @change-component="changeSelectedComponent"
  >
  </nav-bar>
  
  <keep-alive include="class-view">
    <component 
      :is="selectedComponent"
      v-bind="currentProps"
    >
    </component>
  </keep-alive>
  
</template>

<script>

import ClassView from './components/ClassView.vue'
import SelectionList from './components/SelectionList.vue'
import NavBar from './components/navigation/NavBar.vue'

export default {
  name: 'App',
  components: {
    ClassView,
    SelectionList,
    NavBar
  },
  data() {
    return {
      selectedComponent: 'class-view'
    }
  },
  computed: {
    currentProps() {
      if(this.selectedComponent == "selection-list"){
        return { selection: this.selectedComponent }
      }
      return false
    }
  },
  methods: {
    changeSelectedComponent(value){
      this.selectedComponent = value
    }
  }
}
</script>

<style>
 
</style>
