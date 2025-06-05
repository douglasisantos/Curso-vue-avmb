<template>
  <ul>
    <li>
      <a href="#">Home</a>
      <a href="#">Projetos</a>
      <a href="#">Contatos</a>
    </li>
    <li v-if="esta_logado"><a href="#">Meu Perfil</a></li>
  </ul>
</template>

<script setup lang="ts">
defineProps<{
  esta_logado: boolean
}>()
</script>

<style scoped>
ul {
  list-style: none;
  display: flex;
  background-color: #999;
}
li {
  margin-right: 10px;
}
a {
  text-decoration: none;
  color: #ddd;
  transition: 0.5s;
}
a:hover {
  color: turquoise;
}
</style>
