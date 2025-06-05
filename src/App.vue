<template>
  <Header :esta_logado="true" />
  <PrimeiroComponente />
  <p class="paragrafo-pai">O dado de app é</p>
  <LifeCycle />
  <Pessoa />
</template>

<script>
import Header from './components/Header.vue';
import PrimeiroComponente from './components/PrimeiroComponente.vue';
import LifeCycle from './components/LifeCycle.vue';
import Pessoa from './components/Pessoa.vue';

export default {
  name: 'App',
  components: {
    Header,
    PrimeiroComponente,
    LifeCycle,
    Pessoa
  }
}
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
  background-color: #2f00ff;
  padding: 5px;
  border-radius: 4px;
}

.paragrafo-pai {
  color: #00ff4c;
  font-size: 18px;
}
</style>
