<script setup lang="ts">
import Button from '@/components/ui/button/Button.vue';
import {
  Dialog,
  DialogContent,
  DialogDescription,
  DialogHeader,
  DialogTitle,
  DialogTrigger,
} from '@/components/ui/dialog'
import { Input } from '@/components/ui/input'
import { ref, watch } from 'vue';

const dialogApertEst = ref<boolean>(false);
  const quaestio = ref<string>('');

 

</script>

<template>
  <div class="bg-domus-navy h-screen text-white font-sans text-center flex flex-col items-center justify-center gap-12 fixed w-screen overflow-hidden">

  <img class= "absolute opacity-20" src="/imagines/tonitrui.png">

  <h1 class=" text-5xl md:text-7xl  lg:text-8xl font-bold pb-5 md:pb-20 z-10 transition-all">
  <span class="text-domus-cyan">Diseño</span> Web y
  <br/> 
  Apps <span class="text-domus-cyan"> Interactivas </span>
  </h1>

<p class="text-lg md:text-2xl transition-all"> 
Aprendiendo a crear apli caciones web
</p>
    <div class= "scale-z-10">
 <Dialog :open="dialogApertEst"
 @update:open="dialogApertEst = $event"
 >
      <DialogTrigger as-child>
        <Button variant="domus" class="mr-2">
          Sí o no
            </Button>
      </DialogTrigger>
      <DialogContent class="sm:max-w-[425px] bg-domus-navy text-white border-2 border-domus-cyan">
        <DialogHeader>
          <DialogTitle class="text-white">Pregúntame lo que quieras</DialogTitle>
          <DialogDescription class="text-gray-300">
           No sigas con tus dudads yo te responderé SÍ o NO.
          </DialogDescription>
        </DialogHeader>
         <div class="mt-4">
          <Input class= "bg-domus-navy text-white placeholder:text-gray-400 placeholder:text-gray-400" placeholder="Escribe tu pregunta aquí..."
          v-model="quaestio" />
        
        </div>
        </DialogContent> 
       
  </Dialog>

      <Button variant="domus" class="mr-2">
        <RouterLink to="/batman">Batman</RouterLink>
      </Button>
      <Button variant="domus" class="mr-2">
        <RouterLink to="/simpsons">Simpsons</RouterLink>
      </Button>
      <Button variant="domus" class="mr-2">
        <a href="https://www.upv.es" target="_blank" rel="noopener noreferrer">UPV</a>
      </Button>
    </div>
  </div>
</template>

