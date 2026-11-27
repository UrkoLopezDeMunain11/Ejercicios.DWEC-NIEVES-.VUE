<script setup>
import { ref } from 'vue'


const contador = ref(0) // tiene que empezar en 0 el contador


const incrementar = () => {// para boton de incrementar
  contador.value++
}

const decrementar = () => {// para boton de decrementar
  contador.value--
}

const restablecer = () => {// para boton de restablecer a 0 que es como tiene que empezar el contador
  contador.value = 0
}
</script>

<template>
  <p>Contador: {{ contador }}</p> <!-- el contador que quiero q empiece en 2-->
  <button @click="incrementar">Incrementar</button>
  <button @click="decrementar">Decrementar</button>
  <button @click="restablecer">Restablecer</button>
</template>