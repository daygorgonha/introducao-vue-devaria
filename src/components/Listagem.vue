<script lang="ts">
  import { defineComponent } from 'vue';
  export default defineComponent({
    data(){
      return {
        lista: [
          {_id: '12345', nome: 'Usuario 1', login: 'usuario1'},
          {_id: '54321', nome: 'Usuario 2', login: 'usuario2'},
          {_id: '12134', nome: 'Usuario 3', login: 'usuario3'},
          {_id: '13145', nome: 'Usuario 4', login: 'usuario4'},
        ]
      }
    }
  });
</script>

<template>
  <li v-for="item in lista" :key="item._id">
    Usuario: {{item.nome}} - Login: {{item.login}}
  </li>
</template>