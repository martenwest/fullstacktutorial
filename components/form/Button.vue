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
      const { name, rating } = pizzaForm.value
      alert(`${name} rates pizzas a whopping ${rating}`)
    }

    return { send }
  },
})
</script>
