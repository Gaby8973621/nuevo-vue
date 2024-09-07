<template>
  <h1>Primer componente</h1>

  <h1 class="text-3xl font-bold underline">Hello world!</h1>
  <section>
    <h3>numero - {{ numero }}</h3>
    <h3>Multiplicacion {{ contador }}</h3>
  </section>

  <button @click="numero++">+1</button>
  <button @click="numero--">-1</button>
</template>

<script lang="ts" setup>
import { computed, ref } from 'vue'

//DEFINE EL PROPS
interface Props {
  value: number
}
const props = defineProps<Props>()

const numero = ref(props.value)
//FINALISA EL PROPS

const contador = computed(() => numero.value * numero.value)
</script>
<style scoped>
h3 {
  color: red;
}
</style>
