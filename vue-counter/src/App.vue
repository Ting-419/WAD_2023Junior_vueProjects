<script setup>
import TheHeader from './components/TheHeader.vue'
import TheMain from './components/TheMain.vue'
import TheFooter from './components/TheFooter.vue'
</script>

<template>

<div class="flexed">
<TheHeader />

<TheMain />

<TheFooter />
</div>
</template>

<style scoped>
.flexed {
  display: flex;
  flex-direction: column;
  min-height: 100%;
}
</style>
