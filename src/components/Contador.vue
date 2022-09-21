<script lang="ts">
import { defineComponent } from 'vue';
export default defineComponent({
  data() {
    return {
      segundo: 0,
      minuto: 0,
      hora: 0,
      isCincoSegundos: false,
      isDezSegundos: false,
    }
  },
  mounted(){
    setInterval(() => {
      if(this.segundo >= 59){
        this.segundo = 0;
        this.minuto++;

        if(this.minuto >= 59){
        this.minuto = 0;
        this.hora++;
        }else{
          this.minuto++;
        }
      }else{
        this.segundo++
      }

      if(this.hora >= 23){
        this.hora = 0;
        this.minuto = 0;
        this.segundo = 0;
      }

      if(this.segundo % 10 === 0){
        this.isDezSegundos = true; 
        this.isCincoSegundos = false; 
      }else if(this.segundo % 5 === 0){
        this.isCincoSegundos = true; 
        this.isDezSegundos = false; 
      }else{
        this.isCincoSegundos = false; 
        this.isDezSegundos = false;
      }
    },1000);
  },
});
</script>

<template>
  <div>
      <h2 :class="{ 'cinco-segundos': isCincoSegundos, 'dez-segundos': isDezSegundos }">Hora: {{hora}} Minuto: {{minuto}} Segundo: {{segundo}}</h2>
  </div>
</template>

<style scoped>
div{
  display: flex;
  flex-direction: row;
  margin-top: 20px;
}

.dez-segundos{
  color:blueviolet;
}

.cinco-segundos{
  color:brown;
}
</style>