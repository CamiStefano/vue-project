<script setup>
const name = "Vue dinamico";
const styleColor = "color: blue";
const arrayColores = ["blue", "red", "peru"];
const activo = false;

const arrayFrutas = ["🍎", "🍌", "🍉", "🍓", "🍒"];
</script>

<template>
  <h1>Hola {{ name.toUpperCase() }}</h1>
  <h2>{{ arrayColores }}</h2>
  <h2 :style="`color: ${arrayColores[2]}`">Soy peru</h2>
  <h2>{{ activo ? "estoy activo con operador ternario" : " estoy activo con operador ternario" }}</h2>
  <p v-if="activo === true">
    <span>Icono</span>
    Estoy activo
  </p>
  <p v-else-if="activo === false">Estoy inactivo</p>
  <p v-else>Estoy indeciso</p>

  <h2 v-show="activo">Estoy activo v-show</h2>

  <p>{{ arrayFrutas }}</p>

  <ul>
    <li v-for="(fruta, index) in arrayFrutas" :key="index">{{ index }} {{ fruta }}</li>
  </ul>
</template>

<style>
h1 {
  color: peru;
}
</style>
