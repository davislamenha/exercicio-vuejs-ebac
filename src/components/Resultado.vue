<script setup>
const props = defineProps(['result']);
</script>

<template>
  <div class="container text-center">
    <h3 v-if="props.result">Resultado</h3>
    <p class="fs-5" v-else>Aguardando preenchimento dos dados . . .</p>
    <div class="p-5 bg-warning rounded col-md-6 m-auto">
      <div v-if="props.result">
        <span class="h1">{{ props.result }}</span>
      </div>
      <div v-else class="spinner-border" role="status">
        <span class="visually-hidden"></span>
      </div>
    </div>
  </div>
</template>
