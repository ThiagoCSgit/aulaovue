<script setup>
import { ref } from "vue";
const nome = ref("Thiago");
const idade = ref(23);

function fazerAniversario() {
  idade.value += 1;
}

function mudarNome() {
  nome.value = "Thiago Correa";
}
</script>

<template>
  <div class="componente">
    <h1>Componente com dados reativos primitivos</h1>
    <p>Nome: {{ nome }} | Idade: {{ idade }}</p>
    <button @click="fazerAniversario">Fazer Aniversario</button>
    <button @click="mudarNome">Mudar nome</button>
  </div>
</template>

<style></style>
