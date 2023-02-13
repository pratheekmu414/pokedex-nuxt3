<template>
  
  <div :style="image">
    <slot />
  </div>
</template>

<script>
import { VueHeadMixin } from '@unhead/vue';

export default {
  data() {
    return {
      image: { 
    
        backgroundImage: `url(img/background.jpeg)`,	
        backgroundRepeat : "no-repeat",
        backgroundSize: "100vw 100vh",
        backgroundAttachment: "fixed",
        contain:'content',
        height: "100vh",
        overflowY:'scroll',
        overflowX:'hidden'
      }
    };
  }
};
</script>

<style>

</style>