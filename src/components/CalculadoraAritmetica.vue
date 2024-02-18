<script setup>
import { reactive } from 'vue';

const estado = reactive({
  num1: 0,
  num2 : 0,
  operacao: '',
  resultado: '',
})

function somar(num1, num2) {
  estado.resultado = num1 + num2
}

function subtrair(num1, num2) {
  estado.resultado = num1 - num2
}

function multiplicar(num1, num2) {
  estado.resultado = num1 * num2
}

function dividir(num1, num2) {
  estado.resultado = num1 / num2
}

</script>

<template>
  <body>
    <header class="col-md-12 text-center pt-3">
    <h1>Calculadora Aritmetica</h1>
  </header>
  <main>
    <form class="row d-block  my-auto" >
      <label class="col-md-6" for="num1">Insira o primeiro numero</label>
      <input class="col-md-6" v-model="estado.num1" type="number" id="num1" placeholder="insira o 1º numero">
      <label class="col-md-6" for="num2">Insira o segundo numero</label>
      <input class="col-md-6" v-model="estado.num2" type="number" id="num2" placeholder="insira o 2º numero">
      <div class="row">
        <select v-model="estado.operacao" class="col-md-4 text-center mx-auto" >
          <option value="somar">+</option>
          <option value="subtrair">-</option>
          <option value="multiplicar">*</option>
          <option value="dividir">/</option>
        </select>

        <input type="number" v-num1="numero2">

        <p>Resultado: {{ resultado }}</p>
        
      </div>
      <div class="row mt-3">
        <p v-if="estado.operacao === 'somar'"> {{ somar(estado.num1, estado.num2) }} {{ estado.resultado }} </p>
        <p v-else-if="estado.operacao === 'subtrair'"> {{ subtrair(estado.num1, estado.num2) }} {{ estado.resultado }}</p>
        <p v-else-if="estado.operacao === 'multiplicar'"> {{  multiplicar(estado.num1, estado.num2) }}{{ estado.resultado }} </p>
        <p v-else-if="estado.operacao === 'dividir'"> {{ dividir(estado.num1, estado.num2) }} {{ estado.resultado }}</p>
      </div>
    </form>
  </main>
  </body>
</template>

<style scoped>
  body {
    background-color: rgb(193, 21, 216);
  }
</style>