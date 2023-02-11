<template>
  <div class="chat-notification">
    <img :src=imageUrl alt="image" class="pokemon-image">
    <div class="pokemon-name">
      <div>{{ name }}</div>
    </div>
  </div>
</template>
  
<script>
export default {
  props: ['name', 'imageUrl']
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

.chat-notification {
  display: flex;
  width: 15vw;
  height: 30vh;
  contain: content;
  border-radius: 0.5rem;
  color: white;
  flex-direction: column;
  box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);

}

@media (min-width: 0px) and (max-width: 750px) {
  .chat-notification {
    width: 22vw;
  }
}
</style>