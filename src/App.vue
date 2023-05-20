<script setup>
import { reactive } from 'vue';
import Header from './components/Header.vue';
import CalcForm from './components/CalcForm.vue';
import Resultado from './components/Resultado.vue';

const calc = reactive({
  number_1: '',
  number_2: '',
  operator: '',
});

function calcular() {
  const { number_1, number_2, operator } = calc;
  if (number_1 && number_2 && operator) {
    const resultado = eval(`${number_1}${operator}${number_2}`);
    return resultado;
  } else return 0;
}
</script>

<template>
  <Header />
  <CalcForm
    :save-number="
      ({ target }) => {
        calc[target.id] = target.value;
      }
    "
    :save-operator="({ target }) => (calc.operator = target.value)"
  />
  <Resultado :result="calcular()" />
</template>

<style scoped></style>
