<script setup>
  import Navigation  from './components/Navigation.vue'
  import Search  from './components/Search.vue'
  import WeatherCard  from './components/WeatherCard.vue'
  import WeatherCard2  from './components/WeatherCard2.vue'
  
</script>

<template>
  
  <Navigation />

  <div class="text-2xl md:text-4xl text-center text-white font-medium flex items-center justify-center my-20">
    <h1>
      Seeing the weather of the whole world <br> with 
      <span class="bg-clip-text text-transparent font-bold bg-gradient-to-r from-[#CAECFF] to-[#78CFFF]">
        Dark Weather!
      </span>  
    </h1>
  </div>

  <Search />

  <div class="w-full grid md:grid-cols-2 gap-10 lg:grid-cols-3 gap-y-12 lg:gap-y-0 mt-20">
    <WeatherCard city="Dar es Salaam"/>
    <WeatherCard city="Arusha"/>
    <WeatherCard city="Njombe"/>
    <!-- <WeatherCard2 city="Arusha"/>
    <WeatherCard2 city="Njombe"/> -->
  </div>


</template>

