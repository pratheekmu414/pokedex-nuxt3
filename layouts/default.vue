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
    
        backgroundImage: "url(https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTjQkkG7BYTByHkxt__EC3sLLphxIXfTnTcwQ&usqp=CAU)",	
        backgroundRepeat : "no-repeat",
        backgroundSize: "100% 100vh",
        backgroundAttachment: "fixed",
        display:"flex",
        flexDirection:"row",
        justifyContent:"center",
        position:"sticky"
      }
    };
  }
};
</script>

<style>

</style>