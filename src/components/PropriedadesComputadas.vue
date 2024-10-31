<script setup>
import { ref, computed } from "vue";

const anoNascimento = ref(1900);
const anoAtual = ref(2000);
const idade = computed(() => {
  return anoAtual.value - anoNascimento.value;
});
</script>

<template>
  <div class="componente">
    <h1>Componente com propriedades computadas</h1>
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
