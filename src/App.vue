<script setup lang="ts">
  import HelloWorld from './components/HelloWorld.vue';
  import Contador from './components/Contador.vue';
  import DataHora from './components/DataHora.vue';
  import ClassificacaoEtaria from './components/ClassificacaoEtaria.vue';
  import Listagem from './components/Listagem.vue';
  import Formulario from './components/Formulario.vue';
</script>

<template>
  <header>
    <HelloWorld/>
    <Contador/>
    <DataHora/>
    <ClassificacaoEtaria :idade="12"/>
    <Listagem />
    <Formulario />
  </header>
</template>

<style scoped>
header {
  line-height: 1.5;
}
</style>