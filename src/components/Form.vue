<template>
  <div>
    <p>Este é o formulário de cadastro</p>
    <form @submit.prevent>
      <div><InputText /></div>
      <div><InputText /></div>
      <div><SubmitButton /></div>
    </form>
  </div>
</template>

<script setup lang="ts">
import InputText from './Form/InputText.vue'
import SubmitButton from './Form/Submit.vue'
</script>
