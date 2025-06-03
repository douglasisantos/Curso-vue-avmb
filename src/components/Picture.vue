<template>
  <img :src="avatar" :alt="descricao" />
</template>

<script setup lang="ts">
import avatar from '@/assets/avatar.png'

const descricao = 'vampiro'
</script>
