<template>
  <div>
    <button @click="emit('mudarImagem')">Mudar Imagem</button>
  </div>
</template>

<script setup lang="ts">
const emit = defineEmits<{
  (e: 'mudarImagem'): void
}>()
</script>
