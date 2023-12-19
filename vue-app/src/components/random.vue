<template>
    <div>
        <h1>Random!</h1>
        <p>The current random value is: {{ randomValue }}</p>
        <button @click="generateValue">Generate</button>
    </div> 
</template>

<script>
    export default {
        name: "Random",
        data () {
            return{
                randomValue:0
            }
        },
        methods:{
            generateValue(){
                this.randomValue = parseInt(Math.random()*100)
                this.$emit('randomValueIsGenerated',this.randomValue)
            }
        }
    }
</script>