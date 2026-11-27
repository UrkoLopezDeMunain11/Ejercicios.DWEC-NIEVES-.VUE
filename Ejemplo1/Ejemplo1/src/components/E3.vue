<script setup>
import { reactive, computed } from 'vue'

// objeto reactivo con datos del jugador
const jugador = reactive({
  nombre: 'Pepe',
  puntos: 10,
  nivel: 1
})

// cambia el nombre nivel y untos 
const resumen = computed(() => {
  return `${jugador.nombre} — Nivel ${jugador.nivel} (${jugador.puntos} pts)`
})

// 3. Función para sumar 15 puntos al jugador
const sumarPuntos = () => {
  jugador.puntos += 15
}
</script>

<template>
  <p>{{ resumen }}</p>
  <button @click="sumarPuntos">+15 puntos</button>
</template>