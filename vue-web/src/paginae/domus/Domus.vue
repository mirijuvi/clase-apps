<script setup lang="ts">
import Button from '@/components/ui/button/Button.vue';


</script>

<template>
  <div class="fondo-home">

  <h1>
  <span>Diseño</span> Web y
  <br/> 
  Apps <span> Interactivas </span>
  </h1>
    <div class="botones">
      <Button variant="default">
        <RouterLink to="/indecision">Sí o No</RouterLink>
      </Button>
      <Button variant="default">
        <RouterLink to="/batman">Batman</RouterLink>
      </Button>
      <Button variant="default">
        <RouterLink to="/simpsons">Simpsons</RouterLink>
      </Button>
      <Button variant="default">
        <a href:="https://www.upv.es">UPV</a>
      </Button>
    </div>
  </div>
</template>

<style scoped>
.fondo-home{
  background-color: rgb(182, 169, 169);
  height: 100vh;
  color: wheat
}

.botones > Button {
  background-color: pink;
  margin-right: 0.5rem ;
 
}

.botones > Button:hover {
background-color: rgb(208, 159, 255);

}
</style>