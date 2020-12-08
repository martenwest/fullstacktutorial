<template>
  <div class="space-y-4">
    <h1 class="text-lg font-semibold text-gray-800">
      Enter this form to join the pizza club
    </h1>

    <base-label label="Name" message="Enter your name to join the pizza club">
      <base-text-input v-model="pizzaForm.name" />
    </base-label>

    <base-label label="Pizza topping" message="What is your favorite topping?">
      <base-text-input v-model="pizzaForm.topping" />
    </base-label>

    <div class="pt-4 border-t border-gray-600">
      <p>Results</p>

      <span class="block"> name: {{ pizzaForm.name }} </span>
      <span class="block"> topping: {{ pizzaForm.topping }} </span>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'

import { pizzaForm } from '~/state/pizzaForm'

export default defineComponent({
  setup() {
    return {
      pizzaForm,
    }
  },
})
</script>
