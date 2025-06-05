<template>
  <div>
    <button @click="ativarMultiplosEventos">Ativar Múltiplos Eventos</button>
    <p>{{ multiplosEventos }}</p>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const multiplosEventos = ref('')

function primeiro() {
  multiplosEventos.value = 'Primeiro evento ativado'
}

function segundo() {
  setTimeout(() => {
    multiplosEventos.value = 'Segundo evento ativado'
  }, 500)
}

function terceiro() {
  setTimeout(() => {
    multiplosEventos.value = 'Terceiro evento ativado'
  }, 1100)
}

function ativarMultiplosEventos() {
  primeiro()
  segundo()
  terceiro()
}
</script>

<style scoped>
div {
  margin: 100px;
}
</style>
