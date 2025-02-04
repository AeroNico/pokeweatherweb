<template>
    <div class="wanted">
      <h2>Se busca</h2>
      <p>{{ description }}</p>
      <div class="pokemon-grid">
        <img v-for="n in 6" :key="n" :src="pokemonImage" alt="Wanted Pokemon">
      </div>
    </div>
  </template>
  
  <script setup>
  import { defineProps } from 'vue'

  defineProps({
    description: String,
    pokemonImage: String
  });
  </script>
  
  <style scoped>
  .wanted {
    background-color: var(--card-background);
    padding: 16px;
    border-radius: var(--border-radius);
  }
  
  .pokemon-grid {
    display: flex;
    justify-content: center;
    gap: 8px;
  }
  </style>
  