<template>
  <div>
    <h1>Olá Vue!</h1>
    <p>Meu nome é {{ nome }} e trabalho como {{ profissao }}</p>
  </div>
</template>

<script setup lang="ts">
// import { ref } from 'vue'

const nome = ('Douglas')
const profissao = ('Programador')
</script>
