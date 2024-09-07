<template>
  <h1>Mi App</h1>
  <hr />
  <MiComponente :value="5" />
  <MiComponente2 :value="1" />
</template>

<script setup lang="ts">
import MiComponente from './components/MiComponente.vue'
import MiComponente2 from './components/MiComponente2.vue'
</script>

<style scoped></style>
