<template>
  <div class="pokemon-card-container">
    <img :src=imageUrl alt="image" class="pokemon-image">
    <div class="pokemon-name">
      <div>{{ name }}</div>
    </div>  
  </div> 
</template>
  
<script>
export default {
    props: ["name", "imageUrl"],
}
</script>

<style>
.pokemon-name {
  display: flex;
  flex-direction: row;
  justify-content: center;
  background-color: red;
  height: 20%;
}

.pokemon-image {
  width: 100%;
  height: 80%;
  background-color: rgba(165, 225, 242, 0.3);
  display: flex;
  flex-direction: row;
  justify-content: center;
}

.pokemon-card-container {
  display: flex;
  width: 30vh;
  height: 20vw;
  contain: content;
  border-radius: 0.5rem;
  color: white;
  flex-direction: column;
  box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);

}

@media (min-width: 0px) and (max-width: 750px) {
  .pokemon-card-container {
    height: 18vh;
    width: 18vw;
  }

  .pokemon-image {
    width: 100%;
    height: 80%;
    background-color: rgba(165, 225, 242, 0.3);
    display: flex;
    flex-direction: row;
    justify-content: center;
  }


}
</style>