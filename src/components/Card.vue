<!-- Card Component -->
<template>
  <div id="card">
      <img v-if="!reveal" :src="back" alt="">

       <img v-else :src="front" alt="">
  </div>
</template>

<script setup>

// Definir propiedades del componente
// La función recibe un parámetro que es un objeto con todas las propiedades del componente
// Se pone nombredelapropiedad: tipo de variable

const props = defineProps({
    back: String, // es una ruta de img
    front: String, // es una ruta
    reveal: Boolean
})

</script>

<style scoped>
img {
    width: clamp(69px, 18vw, 175px);
}
</style>