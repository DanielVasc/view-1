<!-- aula 1 -->

<!-- <script setup>
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
</template> -->





<!-- aula 2 -->

<script setup>
import { ref } from 'vue';

const contador = ref(0);
const nome = 'Daniel'
const idade = 16

function inverter(texto) {
  return texto.split('').reverse().join('')
}

function saudacao() {
  return `Olá, ${nome}!`
}

function incrementar() {
  contador.value++;
}

function decrementar() {
  if (contador.value > 0) {
    contador.value--;
  }
}

function reiniciar() {
  contador.value = 0;
}

function maior(){
  if(contador > 10){
  
  }
}

</script>

<template>

  <div class="info">
    <h1>Exemplo 1 - Mostrando informações na tela</h1>
    <p>Nome: {{ nome }} </p>
    <p>Idade: {{ idade }} anos</p>
    <hr />
    <p>Para completar 50 anos faltam: {{ 50 - idade }} anos</p>
    <p>O nome tem {{ nome.length }} caracteres</p>
    <p>O nome invertido é: {{ inverter(nome) }} </p>
    <hr />
    <p> Exemplo de saudação usando função</p>
    <p> {{ saudacao() }} </p>
  </div>

  <div class="contador">
    <h1>Contador</h1>
    <p :color="red"> {{ contador }} </p>
    <button @click="incrementar">Incrementar</button>
    <button @click="decrementar">Decrementar</button>
    <button @click="reiniciar">Reiniciar</button>
  </div>

</template>


   

<style scoped>
.info {
  background-color: rgba(35, 12, 22, 1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
}

.contador {
  background-color: rgba(35, 12, 22, 1);
  padding: 20px 30px;
  color: rgb(183, 210, 219);
  border-radius: 10px;
}

.contador p{
  color: aliceblue;
}

h1 {
  color: white;
  font-weight: bold;
  font-size: 1.5em;
}
</style>
