<script setup>
import HelloWorld from './components/HelloWorld.vue'
import TheWelcome from './components/TheWelcome.vue'

import { ref, computed } from 'vue'

// crear contador reactivo que empiece en 0
const contador = ref(0)

// crear propiedad computada que devuelve el doble
const doble = computed(() => {
  return contador.value * 2
})

// funcion incrementar contador al hacer clic
const incrementar = () => {
  contador.value++
}
</script>

<template>
  <p>Contador: {{ contador }} </p><br>
  <p>Doble: {{ doble }} </p><br>
  <button @click= "incrementar">Incrementar</button>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
