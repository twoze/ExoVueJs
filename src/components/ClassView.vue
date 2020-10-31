<template>
  <selection-box
    :selection="selection"
  >
  </selection-box>

  <class-card 
    v-for="(myClass, index) in classdev.classes"
    :key="index"
    :myClass="myClass"
    @add-class="addClassToSelection"
    >
  </class-card>
    
</template>

<script>
import classData from '../data/a3dw1Classes.json'
import ClassCard from './ClassCard.vue'
import SelectionBox from './SelectionBox.vue'

export default {
  name: "class-view",
  components: {
    ClassCard,
    SelectionBox
  },
  data() {
    return {
      classdev: classData,
      selection: []
    }
  },
  methods: {
    addClassToSelection(mclass){
      this.selection.push(mclass)
    }
  }
}
</script>

<style>

</style>