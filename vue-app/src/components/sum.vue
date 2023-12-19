<template>
    <div>
        <h3 >Sum of Sum.vue: {{ sumValue }}</h3> 
    </div> 
</template>

<script>
   export default {
        name: "Sum",
        props:["valueList"],
        components:{History},
        data(){
            return{
                sumValue:0,
                count:0
            }
        },
        watch:{
                valueList: {
                            handler() { this.sumOfSumVue() },
                        }
        },
        methods:{
            sumOfSumVue(){
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