<script setup>
const props = defineProps(['saveNumber', 'saveOperator']);
</script>

<template>
  <form class="container py-5">
    <div class="row flex justify-content-center">
      <div class="col-md-4">
        <input
          @keyup="props.saveNumber"
          type="number"
          id="number_1"
          class="form-control mb-3"
          placeholder="Digite um número"
        />
        <input
          @keyup="props.saveNumber"
          type="number"
          id="number_2"
          class="form-control mb-3"
          placeholder="Digite um número"
        />
      </div>
      <div class="col-md-auto">
        <select @change="props.saveOperator" class="form-select">
          <option selected>Selecione uma opção</option>
          <option value="+">Somar</option>
          <option value="-">Subtrair</option>
          <option value="*">Multiplicar</option>
          <option value="/">Dividir</option>
        </select>
      </div>
    </div>
  </form>
</template>
