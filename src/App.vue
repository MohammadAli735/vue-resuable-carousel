<script setup>
import Carousel from './components/Carousel.vue'
const photots = [
  "src/assets/1.jpg",
  "src/assets/2.jpg",
  "src/assets/3.jpg",
  "src/assets/4.png",
]
// note in real world usage you may get all images with an api call 
</script>


<template>
  <main>
    <Carousel :photots="photots" />
  </main>
</template>

<style >
body {
  background-color: rgba(177, 230, 248, 0.7);
}
</style>
