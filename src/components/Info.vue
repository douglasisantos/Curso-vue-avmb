<template>
  <div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
    <p v-else>Não estou trabalhando no momento.</p>

    <p>Utilizo as seguintes tecnologias para back-end:</p>
    <ul>
      <li v-for="(tecnologia, index) in backend_technologies" :key="index">{{ tecnologia }}</li>
    </ul>

    <p>Utilizo as seguintes tecnologias para front-end:</p>
    <ul>
      <li v-for="tecnologia in frontend_technologies" :key="tecnologia.id">{{ tecnologia.language }}</li>
    </ul>

    <div>
      <button @click="showEmail">{{ textoBotao }}</button>
    </div>
    <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>

    <p class="teste">
      Para acessar meu portfólio basta
      <a :href="meu_link" target="_blank">clicar aqui</a>
    </p>

    <Picture />
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import Picture from './Picture.vue'

const props = defineProps<{
  email: string
  esta_trabalhando: boolean
}>()

const mostrar_email = ref(false)
const textoBotao = ref('Mostrar email')
const meu_link = 'https://google.com'

const backend_technologies = ['Python', 'JavaScript']
const frontend_technologies = [
  { id: 1, language: 'Vue.js' },
  { id: 2, language: 'JavaScript' },
  { id: 3, language: 'HTML' },
  { id: 4, language: 'CSS' }
]

function showEmail() {
  mostrar_email.value = !mostrar_email.value
  textoBotao.value = mostrar_email.value ? 'Esconder email' : 'Mostrar email'
}
</script>

<style>
.paragrafo-pai {
  color: #00ff4c;
}
</style>
