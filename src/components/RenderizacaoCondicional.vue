<script setup>
import { defineProps } from "vue";

defineProps({
  nome: String,
  quantCaes: Number,
});
</script>

<template>
  <div class="componente">
    <h1>Renderização condicional</h1>
    <p>Nome: {{ nome }}</p>
    <p v-if="quantCaes == 0">{{ nome }} não tem catchoros</p>
    <p v-else-if="quantCaes == 1">{{ nome }} tem um catchoro</p>
    <p v-else>{{ nome }} tem muitos catchoros</p>
  </div>
</template>
