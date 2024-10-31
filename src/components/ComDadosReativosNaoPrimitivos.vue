<!-- Composition api -->
<!-- <script setup>
import { reactive } from "vue";

const pessoa = reactive({ nome: "Thiago", idade: 23 });

function fazerAniversario() {
  pessoa.idade += 1;
}

function mudarNome() {
  pessoa.nome = "Thiago Correa";
}
</script> -->

<!-- Options api -->
<script>
export default {
  data: function () {
    return {
      pessoa: {
        nome: "Thiago",
        idade: 23,
      },
    };
  },
  methods: {
    fazerAniversario: function () {
      this.pessoa.idade += 1;
    },
    mudarNome: function () {
      this.pessoa.nome = "Thiago Correa";
    },
  },
};
</script>

<template>
  <div class="componente">
    <h1>Componente com dados reativos não primitivos</h1>
    <p>Nome: {{ pessoa.nome }} | Idade: {{ pessoa.idade }}</p>
    <button @click="fazerAniversario">Fazer Aniversario</button>
    <button @click="mudarNome">Mudar nome</button>
  </div>
</template>

<style></style>
