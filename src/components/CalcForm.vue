<script setup></script>

<template>
  <form class="container py-5">
    <div class="row flex justify-content-center">
      <div class="col-md-4">
        <input
          type="number"
          class="form-control mb-3"
          placeholder="Digite um número"
        />
        <input
          type="number"
          class="form-control"
          placeholder="Digite um número"
        />
      </div>
      <div class="col-auto">
        <select class="form-select">
          <option selected>Selecione uma opção</option>
          <option value="somar">Somar</option>
          <option value="subtrair">Subtrair</option>
          <option value="multiplicar">Multiplicar</option>
          <option value="dividir">Dividir</option>
        </select>
      </div>
    </div>
  </form>
</template>
