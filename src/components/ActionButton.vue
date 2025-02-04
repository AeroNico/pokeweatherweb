<template>
    <button class="action-button">
      <img :src="icon" alt="Button Icon">
      <span>{{ label }}</span>
    </button>
  </template>
  
  <script setup>
  import { defineProps } from 'vue'

  defineProps({
    label: String,
    icon: String
  });
  </script>
  
  <style scoped>
  .action-button {
    display: flex;
    align-items: center;
    background-color: var(--primary-color);
    color: var(--text-light);
    border: none;
    padding: 10px;
    border-radius: var(--border-radius);
    cursor: pointer;
  }
  
  .action-button img {
    margin-right: 8px;
    width: 24px;
  }
  </style>
  