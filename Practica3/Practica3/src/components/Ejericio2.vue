<script setup>
import { ref } from 'vue'

const titulo = ref("");// para que no haya nada en la caja de texto que coje este titulo

</script>

<template>
  <input type="text" placeholder="Escribe algo..."  v-model="titulo"/><!-- el v-model sirve para que al cambiar en la caja de texto se cambie tmabien en el titulo , que vayan juntos lo que se ponga en la caja de texto se pondra en el titulo lo que hara q haya lo mismo en la caja de texto y en HAS escrito:-->
  <p>Has escrito: {{ titulo }}</p> 


</template>