<template >
  <div class="pokemon-details-container">
    <img :src=imageUrl alt="image" class="pokemon-image">
    <div class="pokemon-details-section">
      <div class="pokemon-details-row">
        Name: {{ name }}
      </div>
      <div class="pokemon-details-row">
        Moves: {{ ' '+ details?.moves?.join(', ') }}
      </div>
      <div class="pokemon-details-row">
        Types: {{ ' '+ details?.types?.join(', ') }}
      </div>
      <div class="pokemon-details-row">
        Abilities: {{ ' '+ details?.abilities?.join(', ') }}
      </div>
    </div>
  </div>
</template>
  
<script>

export default {
  props: ['name', 'imageUrl', 'details']
}
</script>

<style>
.pokemon-details-section{
  display: flex;
  flex-direction: column;
justify-content: space-evenly;
height: 80%;
text-transform: capitalize;
}
.pokemon-name {
  display: flex;
  flex-direction: row;
  justify-content: center;
  background-color: rgb(7, 114, 5);
  height: 20%;
  color: rgb(237, 224, 45);
}

.pokemon-details-row {
  display: flex;
  flex-direction: column;
  height: 1em;
  justify-content: space-evenly;

}

.pokemon-image {
  width: 100%;
  height: 60%;
  background-color: rgba(17, 15, 131, 0.3);
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.pokemon-details-container {
  display: flex;
  width: 30vw;
  height: 70vh;
  contain: content;
  border-radius: 0.5rem;
  color: rgb(4, 3, 0);
  background: rgb(255, 255, 255);
  flex-direction: column;
  border: 10px solid rgb(255, 255, 255);
  box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
 
}

@media (min-width: 0px) and (max-width: 750px) {
  .pokemon-details-container {
    width: 60vw;
  height: 70vh;
}
}
</style>