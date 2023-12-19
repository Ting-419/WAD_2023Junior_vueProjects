<template>
    <h2>This is a main of my page</h2>
    <h5>My Counter value = {{ counter }}</h5>
    <div>
        <button @click="incCounter">Increment counter</button>
    </div>
    <h1>My Counter value = {{ counter + r }}</h1>
    <h2>My Counter value = {{ counter + 2 }}</h2>
    <h3>My Counter value = {{ counter + 3 }}</h3>
    <h4>My Counter value = {{ counter + 4 }}</h4>
    <h5>My Counter value = {{ counter + 5 }}</h5>
</template>

<script>
import Counter from './Counter.vue'
export default {
    name: "TheMain",
    data() {
        return {
            counter: 0,
            r: 10
        }
    },
    methods: {
        incCounter() {
            this.counter++;
        }
    }
}
</script>

<style></style>