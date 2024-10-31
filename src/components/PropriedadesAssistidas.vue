<script setup>
// import { ref, watch } from "vue";
import { ref, watchEffect } from "vue";

const anoNascimento = ref(1900);
const anoAtual = ref(2000);
const idade = ref(0);

// watch(anoAtual, (ano) => {
//   idade.value = ano - anoNascimento.value;
// });

// watch(anoNascimento, (ano) => {
//   idade.value = anoAtual.value - ano;
// });

// fuciona igual o watch, mas não precisa passar a variavel que voce quer vigiar
watchEffect(() => {
  idade.value = anoAtual.value - anoNascimento.value;
});
</script>

<template>
  <div class="componente">
    <h1>Componente com propriedades assistidas</h1>
    <p>{{ idade }}</p>
    <div class="form">
      <label for="">ano nascimento:</label>
      <input type="number" v-model="anoNascimento" />
      <label for="">ano atual:</label>
      <input type="number" v-model="anoAtual" />
    </div>
  </div>
</template>

<style scoped>
.form {
  display: flex;
  flex-direction: column;
}

.form label {
  margin-bottom: 10px;
}
</style>
