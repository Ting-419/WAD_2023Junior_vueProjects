<template>
    <div>
        <h1>The List:</h1>
        <p v-for="value in valueList" :style="textRed(value)" >{{ value }}</p>
        <h3>Sum of History.vue: {{ sumValue }}</h3>
    </div>
</template>
<script>
    export default{
        name:"History",
        props:["valueList"],
        data(){
            return{
                sumValue:0,
                count:0
            }
        },
        watch:{
                valueList: {
                            handler() { this.sumOfHistory() },
                        }
        },
        methods:{
            textRed(value){
                if (value > 50){
                    return{color:"red"}
                } else{
                    return{color:"black"}
                }
            },
           
            sumOfHistory(){
                this.count++;
                console.log("cou=" + this.count) 
                this.sumValue = 0;
                for(let i = 0; i < parseInt(this.valueList.length);i++){
                    this.sumValue =parseInt(this.sumValue + this.valueList[i]);
                    console.log("i= " + i)
                    console.log("this.valueList.length= " + this.valueList.length)
                    console.log("value=" + this.valueList[i])
                    console.log("sumValue= " + this.sumValue)
            }
        }
    }
} 
</script>