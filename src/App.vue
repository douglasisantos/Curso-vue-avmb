<template>
  <Header :esta_logado="true" />
  
  <PrimeiroComponente />
  <p class="paragrafo-pai">O dado de app é {{ mensagem }}</p>
  <p v-show="true">{{ mensagem }}</p>
  <LifeCycle />
  <Pessoa />
</template>

<script setup lang="ts">
import Header from './components/Header.vue'
import PrimeiroComponente from './components/PrimeiroComponente.vue'
import LifeCycle from './components/LifeCycle.vue'
import Pessoa from './components/Pessoa.vue'

const mensagem = 'Olá, Vue.js!'
</script>

<style>
body {
  background-color: #333;
  color: #fff;
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

a {
  color: #ff0505;
}

.teste {
  background-color: #00ccff;
  padding: 5px;
  border-radius: 4px;
}

.paragrafo-pai {
  color: #ffffff;
  font-size: 18px;
}
</style>
