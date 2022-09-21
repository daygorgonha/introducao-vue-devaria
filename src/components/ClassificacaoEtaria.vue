<script lang="ts">
  import {defineComponent} from 'vue';
  export default defineComponent({
    props: {
      idade : Number
    }
  })
</script>

<template>
  <h1 v-if="idade && idade <=6">Censura Livre</h1>
  <h1 v-else-if="idade && idade >=6 && idade < 10">Censura 6 anos</h1>
  <h1 v-else-if="idade && idade >=10 && idade < 12">Censura 10 anos</h1>
  <h1 v-else-if="idade && idade >=12 && idade < 16">Censura 12 anos</h1>
  <h1 v-else-if="idade && idade >=16 && idade < 18">Censura 16 anos</h1>
  <h1 v-else-if="idade && idade >=18">Censura 18 anos</h1>
  <h1 v-else>Idade nao informada.</h1>
</template>