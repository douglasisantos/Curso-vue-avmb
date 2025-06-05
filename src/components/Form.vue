<template>
  <div>
    <p>Este é o formulário de cadastro</p>
    <form @submit.prevent="enviarFormulario">
      <input type="text" v-model="name" />
      <input type="text" v-model="email" />
      <div><Submit /></div>
    </form>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import Submit from './Form/Submit.vue'
import InputText from './Form/InputText.vue' // Só importa se usar no template

const name = ref('')
const email = ref('')

function enviarFormulario() {
  console.log('Formulário enviado')
  console.log('Nome:', name.value)
  console.log('Email:', email.value)
}
</script>
