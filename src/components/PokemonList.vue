<template>
    <div class="pokemon-list">
      <h2>Pokémon avistados</h2>
      <div class="grid">
        <div v-for="pokemon in pokemons" :key="pokemon.id" class="pokemon">
          <img :src="pokemon.image" :alt="pokemon.name">
          <p>{{ pokemon.name }}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { defineProps } from 'vue'

  defineProps({
    pokemons: Array // [{ id: 1, name: 'Pokemon0001', image: '...' }]
  });
  </script>
  
  <style scoped>
  .pokemon-list {
    background-color: var(--card-background);
    padding: 16px;
    border-radius: var(--border-radius);
  }
  
  .grid {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }
  
  .pokemon {
    text-align: center;
  }
  </style>
  