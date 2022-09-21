<script lang="ts">
  import {defineComponent} from 'vue';
  export default defineComponent({
    data(){
      return{
        agora: new Date()
      }
    },
    computed:{
      getDataFormatada(){
        return this.agora.getDate() + '/' + (this.agora.getMonth()+1) + '/' + this.agora.getFullYear();
      }
    }
  });
</script>

<template>
  <h2>Data atual: {{getDataFormatada}}</h2>
</template>