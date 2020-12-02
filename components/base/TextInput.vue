<template>
  <input
    :value="value"
    type="text"
    class="w-full h-12 p-2 border-2 border-gray-400 rounded"
    @input="({ target: { value } }) => $emit('input', value)"
  />
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({
  props: {
    value: {
      type: String,
      required: true,
    },
  },
})
</script>
