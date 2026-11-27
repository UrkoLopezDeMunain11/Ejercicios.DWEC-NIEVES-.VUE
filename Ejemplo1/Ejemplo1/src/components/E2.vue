<script setup>
import { ref, computed } from 'vue'

// iniciada en modo apagado
const encendida = ref(false)

// el texto que va a devovler de dentro del boton segun su estado apagada o encendida
const estadoTexto = computed(() => {
  return encendida.value ? 'Encendida' : 'Apagada'
})

// funcion para cambiar ese estado de encendido a apagado
const cambiarEstado = () => {
  encendida.value = !encendida.value
}
</script>

<template>
  <p>Estado: {{ estadoTexto }}</p>
  <button @click="cambiarEstado">Cambiar estado</button>
</template>