<template>
  <div>
    <button @click="ativar">Clique aqui</button>
    <span v-show="ativou">Ativado</span>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'

const ativou = ref(false)

function ativar() {
  ativou.value = !ativou.value
}
</script>
