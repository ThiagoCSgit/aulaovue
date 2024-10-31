<script setup>
import { defineProps } from "vue";

defineProps({
  nome: String,
  cachorros: Array,
});
</script>

<template>
  <div class="componente">
    <h1>Renderização de listas</h1>
    <p>Nome: {{ nome }}</p>
    <p v-show="cachorros.length == 0">Sem catchoros</p>
    <ul>
      <li v-for="(cao, index) in cachorros" :key="index">
        Nome: {{ cao.nome }} | Idade: {{ cao.idade }}
      </li>
    </ul>
  </div>
</template>

<style scoped>
ul {
  margin: 0px;
  padding: 0px;
}

li {
  list-style: none;
  text-align: center;
  font-size: large;
}
</style>
