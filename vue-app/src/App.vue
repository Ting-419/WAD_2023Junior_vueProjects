<template>
  <div id="app">
  <Random @randomValueIsGenerated="onRandomValueIsGenerated"></Random>
  <History :valueList="valueList"></History>
  <Sum :valueList="valueList"></Sum>
  </div>
</template>

<script>
   import Random from "@/components/random.vue"
   import History from "@/components/history.vue"
   import Sum from "@/components/sum.vue"

   export default{
    name:"App",
    components: {Random,History,Sum},
    data(){
      return{
        valueList:[]
      }
    },
    methods:{
      onRandomValueIsGenerated(value){
       this.valueList.push(value)
      }
    }
   }
</script>

<style>
</style>