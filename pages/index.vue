<template >
  <div class="template">

    <!-- search bar -->
    <div class="search"> 
      <input placeholder=' Search Pokemons...' class="search-bar" type="text"  v-on:input="searchPokemon" />
    </div>

    <!-- Grid -->
    <div class="grid">
      <div v-for="(item, index) in pokemons.result">
        <PokemonCard :name=item?.name :imageUrl=item?.image />
      </div>
    </div>

  </div>

</template>

<script setup>
import PokemonCard from '../components/pokemon-card.vue'

const { data: pokemons } = await useFetch('https://pokemon-wrapper-api-pratheek.up.railway.app/pokedex')

const searchPokemon= async (event) => {
const value= event?.target?.value??1;
  const result = await $fetch(`https://pokemon-wrapper-api-pratheek.up.railway.app/pokedex?search=${value}`);
  pokemons.value = result
};

</script>

<style>
.pokedex{
  background-color: green;
}
.template {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
}

.search {
  height: 15vh;
  width: 100%;
  background-color: rgb(236, 26, 26);
  contain: content;
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  margin-bottom: 10vh;
}

.search-bar{
    
  height: 5vh;
  background: rgb(235, 235, 228);
  width: 70vw;
  }

.grid {
  display: grid;
  grid-template-columns: 25vw 25vw 25vw;
  grid-gap: 5vh;
  margin-left: 10vw;
  margin-bottom: 10vh;

}
@media (min-width: 0px) and (max-width: 750px) {
  .chat-notification {
    margin-left: 0vw;
  }
}
</style>