<script setup>
import { ref } from 'vue'


const tareas= ref (["Aprender Vue", "Practicar JS"]);// meto solo las tareas que hay luego al y añadiendo con el boton se iran añadiendo mas tareas al array


const agregarTarea = () => { // para agregar nueva tarea con tareas.value y o de length + 1 es para sumar a las tareas q ya habia una tarea mas con lenth saldra todas las que hay en este caso dos y le sumara otra mas
  tareas.value.push(tareas.value.length + 1)
}


</script>

<template>
  <h4>Mis tareas: ({{ tareas.length }}) </h4>  <!--poruq al lado de ese texto aparecen las tareas que hay asiq poner lenght-->
  <ul>
    <li v-for="(tarea ,index) of tareas" :key="index"> <!--tiene que recorrer todo el array de tareas y ir sacandomelas y ademas en estilo de lista-->
        {{ tarea }}
    </li >
  </ul>
  <button @click="agregarTarea">Añadir tarea</button> 
</template>