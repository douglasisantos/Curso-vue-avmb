<template>
  <div>
    <h2>Esta é a descrição da pessoa: {{ nome }}</h2>
    <Info />
    <Form />
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import Info from './Info.vue'
import Form from './Form.vue'

const nome = ref('Douglas')
</script>
