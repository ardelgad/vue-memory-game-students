<!-- ChessBoard Component -->
<template>
  <!-- Iteración 3: Utiliza adecuadamente el v-for para crear tantas Card como elementos hay en 'cards'. -->
  <div>
    <Card
      v-for="card in cards"
      :key="card.id"
      :back="backCardImage"
      :front="card.image"
      :reveal="true"
    ></Card>
    <Card
      v-for="card in cards"
      :key="card.id"
      :back="backCardImage"
      :front="card.image"
      :reveal="false"
    >
    </Card>
  </div>
</template>

<script setup>
import Card from "./Card.vue";

const props = defineProps({
  cards: Array,
  backCardImage: String,
});
</script>

<style scoped>
div {
  display: grid;
  grid-template-columns: repeat(5, 1fr);
  row-gap: 1rem;
}
</style>