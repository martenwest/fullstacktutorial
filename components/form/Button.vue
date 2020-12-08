<template>
  <button
    class="w-full p-2 font-semibold text-white bg-orange-500 rounded"
    @click="send"
  >
    SEND
  </button>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'

import { pizzaForm } from '~/state/pizzaForm'

export default defineComponent({
  setup() {
    const send = () => {
      const { name, topping } = pizzaForm.value
      alert(`${name}'s favorite topping is ${topping}`)
    }

    return { send }
  },
})
</script>
