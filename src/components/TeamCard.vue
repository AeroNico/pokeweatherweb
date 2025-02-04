<template>
    <div class="team-card">
      <h2>Tu equipo de hoy</h2>
      <div class="grid">
        <div v-for="pokemon in team" :key="pokemon.id" class="team-member">
          <img :src="pokemon.image" alt="Team Pokemon">
          <p>{{ pokemon.name }}</p>
          <p class="type">{{ pokemon.type }}</p>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { defineProps } from 'vue'

  defineProps({
    team: Array // [{ id: 1, name: 'Pokemon', type: 'Volador', image: '...' }]
  });
  </script>
  
  <style scoped>
  .team-card {
    background-color: var(--card-background);
    padding: 16px;
    border-radius: var(--border-radius);
  }
  
  .grid {
    display: flex;
    flex-wrap: wrap;
    gap: 8px;
  }
  
  .team-member {
    text-align: center;
  }
  </style>
  