<template>
  <div>
    <img :src="avatar" :alt="descricao" />
    <MudarImagem @mudarImagem="mudarImagem" />
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import MudarImagem from './MudarImagem.vue'

import avatarInicial from '@/assets/avatar.png'
import avatarAlternativo from '@/assets/avatar2.jpeg'

const avatar = ref(avatarInicial)
const descricao = 'vampiro'

function mudarImagem() {
  avatar.value = avatarAlternativo
}
</script>
