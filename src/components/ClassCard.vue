<template>
  <div 
    class="border m-2 p-2 flex justify-between shadow-md"
    :class="delayStyle"
  >
    <div>
      <h1 class="text-lg font-bold">{{ className }}</h1>
      <p> {{ TeacherUp }} </p>
      <p>{{ isdelay }}</p>
      <img class="max-w-xs	" alt="" src="../assets/img/naruto.jpg">

    </div>
    <base-button
      text="Sélectionner"
      @click="addToSelection"
    >
    </base-button>
  </div>
</template>

<script>


export default {
  name: "class-card",
  props: ['myClass'],
  computed: {
    className(){
      console.log(this.myClass.name.split('.'))
      if(this.myClass.name.split('.').length > 1){
        return this.myClass.name.split('.')[1]
      }
      return this.myClass.name;
    },
    TeacherUp(){
      return this.myClass.teacher.toUpperCase()
    },
    isdelay() {
      return this.myClass.delay
    },
    delayStyle() {
      return { 
        'hover: orange':this.isdelay
      }
    }
  },
  methods: {
    addToSelection() {
      this.$emit('add-class', this.myClass)
    }
  }
}
</script>

<style scoped>
  
</style>