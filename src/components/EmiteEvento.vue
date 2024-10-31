<script setup>
import { defineProps, defineEmits } from "vue";
const props = defineProps({
  item: String,
  preco: Number,
});

const emit = defineEmits(["adicionarProduto"]);

function adicionar() {
  console.log("preco:", props.preco);
  emit("adicionarProduto", props.preco);
}
</script>

<template>
  <div class="componente">
    <h1>Componente que emite evento</h1>
    <p>{{ item }} (R$ {{ preco.toFixed(2) }})</p>
    <button @click="adicionar">Adicionar ao carrinho</button>
  </div>
</template>
