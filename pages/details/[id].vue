<template >
  <div class="pokemon-details-template">
    <div v-for="(item) in pokemons.result">
      <PokemonDetails :name=item?.name :imageUrl=item?.image :details=item?.details />
    </div>
  </div>
</template>

<script setup>
import PokemonDetails from '../../components/pokemon-details.vue'
const route = useRoute() 
const id = route.params.id
const { data: pokemons } = await useFetch(`https://pokemon-wrapper-api-pratheek.up.railway.app/pokedex?pokemon=${id}`)
</script>

<style>
.pokemon-details-template {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 15vh;
  width: 100%;
}

</style>