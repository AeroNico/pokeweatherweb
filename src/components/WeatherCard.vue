<template>
    <div class="weather-card">
      <h2>Clima {{ type }} | <span class="city">{{ city }}</span></h2>
      <img :src="weatherIcon" alt="Weather Icon">
      <p class="condition">{{ condition }}</p>
      <p class="temperature">{{ temperature }}°</p>
    </div>
  </template>
  
  <script setup>
  import { defineProps } from 'vue'

  defineProps({
    type: String,        // 'actual' o 'próximo'
    city: String,
    condition: String,   // 'Despejado', 'Lluvioso', etc.
    temperature: Number,
    weatherIcon: String,
  });
  </script>
  
  <style lang="scss" scoped>
  
  .weather-card {
    background-color: $card-background;
    padding: 16px;
    border-radius: $border-radius;
    text-align: center;
    color: $text-light;
    box-shadow: $shadow;
  
    .city {
      color: $accent-color;
    }
  
    .temperature {
      font-size: 24px;
      color: $primary-color;
    }
  }
  </style>