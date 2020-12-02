<template>
  <div class="space-y-4">
    <h1 class="text-lg font-semibold text-gray-800">
      Enter this form to join the pizza club
    </h1>

    <base-label label="Name" message="Enter your name to join the pizza club">
      <base-text-input v-model="pizzaForm.name" />
    </base-label>

    <base-label
      label="Pizza Rating"
      message="From 1 to 10 how much do you like pizza?"
    >
      <base-number-input v-model="pizzaForm.rating" />
    </base-label>

    <div class="pt-4 border-t border-gray-600">
      <p>Results</p>

      <span class="block"> name: {{ pizzaForm.name }} </span>
      <span class="block"> rating: {{ pizzaForm.rating }} </span>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from '@nuxtjs/composition-api'

export default defineComponent({
  setup() {
    const pizzaForm = ref({
      name: '',
      rating: 0,
    })

    return {
      pizzaForm,
    }
  },
})
</script>
