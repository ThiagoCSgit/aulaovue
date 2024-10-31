<script setup>
import { ref } from "vue";

const valor = ref("Vue é legal");
</script>

<template>
  <div class="componente">
    <h1>Componente com data binding</h1>
    <input type="text" v-model="valor" />
    <p>{{ valor }}</p>
  </div>
</template>
