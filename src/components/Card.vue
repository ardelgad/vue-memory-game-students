<!-- Card Component -->
<template>
  <div id="card">
      <img v-if="!reveal" :src="back" alt="">

       <img v-else :src="front" alt="">
  </div>
</template>

<script setup>
// Iteración 2
// Cread una carta pokemon con el reverso
// La carta muestra el pokemon o el reverso de la carta en función de una variable de estado que se llama reveal const reveal = false;

// Definir propiedades del componente
// La función recibe un parámetro que es un objeto con todas las propiedades del componente
// Se pone nombredelapropiedad: tipo de variable

const props = defineProps({
    back: String, // es una ruta de img
    front: String, // es una ruta
    reveal: Boolean
})

</script>

<style>

</style>