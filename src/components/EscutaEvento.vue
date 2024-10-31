<script setup>
import EmiteEvento from "./EmiteEvento.vue";
import { ref } from "vue";

const total = ref(0);

function atualizarTotal(preco) {
  console.log(preco);
  const valor = total.value + preco;
  total.value = +valor.toFixed(2);
}
</script>

<template>
  <div class="componente">
    <h1>Componente que escuta evento</h1>
    <p>Total: R${{ total }}</p>
    <div class="lista">
      <EmiteEvento
        item="Item1"
        :preco="1.99"
        @adicionarProduto="atualizarTotal"
      />
      <EmiteEvento
        item="Item2"
        :preco="5.0"
        @adicionarProduto="atualizarTotal"
      />
      <EmiteEvento
        item="Item3"
        :preco="10.99"
        @adicionarProduto="atualizarTotal"
      />
    </div>
  </div>
</template>

<style scoped>
.lista {
  display: flex;
  justify-content: space-between;
}
</style>
