<script setup></script>

<template>
  <div class="componente">
    <h1>Slots</h1>
    <button>
      <slot name="icone" />
      <slot name="texto">Botão</slot>
      <!-- caso nada seja passado para o slot texto "Botão" será o valor padrão -->
    </button>
  </div>
</template>
