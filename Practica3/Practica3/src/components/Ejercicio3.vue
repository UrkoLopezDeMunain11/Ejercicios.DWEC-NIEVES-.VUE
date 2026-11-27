<script setup>
import { ref } from 'vue'
import { reactive } from 'vue'

const persona = reactive({// reactive para que vue actulaice los cambios , sin eso no lo hara cuando cambie la edad
    nombre: "Ana",
    edad: 25,
    correo: "ana@example.com"
});

const incrementar = () => {// para boton de incrementar, para que cuando entre aqui vaya a persona edad y la aumente
  persona.edad++
}


</script>

<template>
  <p>Contador: {{ persona.nombre }} ({{ persona.edad }})</p>  <!--para que me muestre lo que tenga eprsona en nombre y en edad-->
  <p>Contador: {{ persona.correo }}</p> <!--para que me muestre lo que enga persona en correo-->
  <button @click="incrementar">Cumplir años</button> <!-- el boton para incremetar que la pulsarle llamara al metodo incrementar que este aumentara la edad de persona-->
</template>