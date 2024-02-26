<script setup>
  import { ref } from 'vue';

  const contador = ref(0);

  //função para adicionar um numero
  function incrementar() {
    contador.value++; 
    // .value é usado para se referir ao valor, Já o ++ usamos para nos referir a aumentar em 1
  }

   //função para tirar um numero
  function decrementar() {
    if (contador.value > 0) {
      contador.value--;
      // mesma logica que o incrementar
    }
  }

   //função para reiniciar, voltar ao 0
  function reiniciar() {
    contador.value = 0;
    //esse codigo faz com que o valor do contador volte para o 0
  }
</script>

<template>
  <div>
    <h1>Contador</h1>
    <p> {{ contador }} </p>
    <button @click="incrementar">Incrementar</button>
    <button @click="decrementar">Decrementar</button>
    <button @click="reiniciar">Reiniciar</button>
  </div>
</template>
