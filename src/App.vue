<script setup>
  import Navigation  from './components/Navigation.vue'
  import Search  from './components/Search.vue'
  import WeatherCard  from './components/WeatherCard.vue'
  
</script>

<template>
  
  <Navigation />

  <div class="text-4xl text-center text-white font-medium flex items-center justify-center my-20">
    <h1>Seeing the weather of the whole world <br> with <span class="bg-clip-text text-transparent font-bold bg-gradient-to-r from-[#CAECFF] to-[#78CFFF]">Dark Weather!</span>  </h1>
  </div>

  <Search />

  <div class="grid grid-cols-3 gap-36 mt-20">
   
    <WeatherCard city="Dar es Salaam" />
    <WeatherCard city="Arusha" />
    <WeatherCard city="Njombe" />
  </div>


</template>

