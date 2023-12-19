<template>
    <h5>My Counter value = {{ counter }}</h5>
</template>

<script>
export default {
    name: "Counter",
    data() {
      return {
        counter: 0
      }
    }
}
</script>