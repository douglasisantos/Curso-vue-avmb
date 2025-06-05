<template>
  <div>
    <h1>Olá Vue!</h1>
    <p>Meu nome é {{ nome }} e trabalho como {{ profissao }}</p>
    <MultiplosEventos />
    <Reutilizacao />
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import MultiplosEventos from './MultiplosEventos.vue'
import Reutilizacao from './Reutilizacao.vue'

const nome = ref('Douglas')
const profissao = ref('Programador')
</script>
