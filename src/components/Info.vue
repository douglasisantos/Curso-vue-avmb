<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Não estou trabalhando no momento.</p>

    <p>Utilizo as seguintes tecnologias:</p>
    <ul>
      <li>Vue.js</li>
      <li>JavaScript</li>
      <li>HTML</li>
      <li>CSS</li>
    </ul>

    <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
    <p>
      Para acessar meu portfólio basta
      <a :href="meu_link" target="_blank">clicar aqui</a>
    </p>

    <Picture />
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import Picture from './Picture.vue'

const esta_trabalhando = ref(true)
const mostrar_email = ref(true)
const email = ref('douglasiracet@gmail.com')
const meu_link = ref('https://google.com')
</script>
