<template>
    <div>
      <Header />
      <WeatherCard type="actual" city="Santiago" condition="Despejado" :temperature="26" :weatherIcon="weatherIconUrl" />
      <PokemonList :pokemons="pokemonAvistados" />
      <WantedPokemon description="..." pokemonImage="ruta_icono.png" />
      <TeamCard :team="equipoHoy" />
      <ActionButton label="Compartir" icon="ruta_icono.png" />
      <ActionButton label="Descargar" icon="ruta_icono.png" />
    </div>
  </template>
  
  <script setup>
  import Header from '@/components/MainHeader.vue';
  import WeatherCard from '@/components/WeatherCard.vue';
  import PokemonList from '@/components/PokemonList.vue';
  import WantedPokemon from '@/components/WantedPokemon.vue';
  import TeamCard from '@/components/TeamCard.vue';
  import ActionButton from '@/components/ActionButton.vue';
  import weatherIcon from '@/assets/placeholder_icon.png'; // Import the SVG


  const weatherIconUrl = weatherIcon; // Use the imported SVG


  const pokemonAvistados = [
    { id: 1, name: "Pokemon0001", image: "ruta_icono.png" },
    // ...
  ];
  
  const equipoHoy = [
    { id: 1, name: "Pokemon", type: "Volador", image: "ruta_icono.png" },
    // ...
  ];
  </script>
  