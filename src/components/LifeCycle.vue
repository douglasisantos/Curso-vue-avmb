<template>
  <h1>Meu nome é : {{ nome }}</h1>
</template>

<script setup lang="ts">
import { ref, onMounted } from 'vue'

// Criamos o estado
const nome = ref('ainda não sei')

// Equivalente ao 'created()'
setTimeout(() => {
  nome.value = 'Douglas'
}, 1000)

// Equivalente ao 'mounted()'
onMounted(() => {
  setTimeout(() => {
    nome.value = 'João'
  }, 2000)
})
</script>
