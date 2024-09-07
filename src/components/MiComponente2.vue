<template>
  <h1>Primer componente</h1>

  <section>
    <h3>numero - {{ numero }}</h3>
    <h3>Multiplicacion {{ contador }}</h3>
  </section>

  <button @click="numero++">+1</button>
  <button @click="numero--">-1</button>
</template>

<script lang="ts">
import { computed, defineComponent, ref } from 'vue'

//DEFINE EL PROPS
export default defineComponent({
  props: {
    value: { type: Number, required: true }
  },
  setup(props) {
    const numero = ref(props.value)
    const contador = computed(() => numero.value * numero.value)

    return {
      numero,
      contador
    }
  }
})

//FINALISA EL PROPS
</script>
<style scoped>
h3 {
  color: red;
}
</style>
