<script setup>
import { ref, computed } from 'vue';

const contador = ref(0);
const contador2 = ref(0);

function incrementar() {
  contador.value++;
}

function incrementar2() {
  contador2.value++;
}

function decrementar() {
  if (contador.value > 0) {
    contador.value--;
  }
}

function decrementar2() {
  if (contador.value > 0) {
    contador.value--;
  }
}

function reiniciar() {
  contador.value = 0;
}

function reiniciar2() {
  contador2.value = 0;
}

let juntar = computed(() => {
  return contador.value + contador2.value
});

let parImpar = computed(() => {
  return juntar.value % 2 === 0 ? 'par' : 'ímpar'
});

const soma = computed(() => {
return contador.value + contador2.value
});
</script>


<template>
  <div class="contador">
    <div class="info">
      <h1>Contador</h1>
      <p :color="red"> {{ contador }} </p>
      <button @click="incrementar">+1</button>
      <button @click="decrementar">-1</button>
      <button @click="reiniciar">Reiniciar</button>
      <div v-if="contador > 10"> o número é maior que 10</div>
      <div v-else>O número é menor que 10 </div>
    </div>
  </div>

  <div class="contador">
    <div class="info">
      <h1>Contador</h1>
      <p :color="red"> {{ contador2 }} </p>
      <button @click="incrementar2">+1</button>
      <button @click="decrementar2">-1</button>
      <button @click="reiniciar2">Reiniciar</button>
      <div v-if="contador2 > 10"> o número é maior que 10</div>
      <div v-else>O número é menor que 10 </div>
    </div>
  </div>

  <div class="Sominha">
    <h1>Soma</h1>
    <p :color="red">{{ soma }}</p>
    <div v-if="contador + contador2 > 10">A soma é maior que 10</div>
    <div v-else>A soma é menor que 10 </div>
  </div>

  <div class="parouimpar">
    <h1>Par ou ímpar</h1>
    <p :color="red">{{ parImpar }}</p>
  </div>

  <div class="booleano">
    <h1>Verdadeiro ou falso</h1>
  <p :color="red">{{ contador + contador2 > 30 ? 'Sim' : 'Não' }}</p>
</div>
</template>

<style scoped>
  .info {
    background-color: rgba(35, 12, 22, 1);
    padding: 40px 50px;
    color: rgb(183, 210, 219);
    border-radius: 10px;
  }

  .contador {
    padding: 20px 30px;
    color: rgb(183, 210, 219);
    border-radius: 10px;
    margin-top: 20px;
  }

  h1 {
    color: white;
    font-weight: bold;
    font-size: 3em;
  }

  .Sominha {
    padding: 20px 30px;
    color: rgb(97, 121, 129);
    border-radius: 10px;
    margin-top: 20px;
  }

  .parouimpar {
    padding: 20px 30px;
    color: rgb(97, 121, 129);
    border-radius: 10px;
    margin-top: 20px;
  }

  .booleano {
    padding: 20px 30px;
    color: rgb(97, 121, 129);
    border-radius: 10px;
    margin-top: 20px;
  }
</style>
