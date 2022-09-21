<script lang="ts">
  import { defineComponent } from 'vue';
  export default defineComponent({
    data(){
      return {
        nome: '',
        data: '',
        categoria: '',
      }
    },
    methods: {
      doClick(){
        alert(`Dados do formulario - nome: ${this.nome}, data: ${this.data}, categoria: ${this.categoria}`);
      },
      limpar(){
        this.nome='';
        this.data='';
        this.categoria='';
      }
    }
  });
</script>

<template>
  <form>
    <div>
      <label name="nome">Nome:</label>
      <input type="text" for="nome" v-model="nome"/>
    </div>
    <div>
      <label name="data">Data de nascimento:</label>
      <input type="date" for="data" v-model="data"/>
    </div>
    <div>
      <label name="categoria">Categoria:</label>
      <select for="categoria" v-model="categoria">
        <option>Aluno</option>
        <option>Professor</option>
        <option>Coordenador</option>
        <option>Diretor</option>
      </select>
    </div>
    <button @click.enter.prevent="doClick">Salvar</button>
    <button @click.prevent="limpar">Limpar</button>
  </form>
</template>

<style scoped>
form{
  margin: 40px 20px;
}

div{
  margin: 10px 0px;
  display: flex;
  flex-direction: row;
}
</style>