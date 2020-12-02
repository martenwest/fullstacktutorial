<template>
  <div class="flex items-center space-x-4 dashed-border">
    <input
      :value="value"
      type="number"
      :min="0"
      class="w-16 h-12 p-2 border-2 border-gray-400 rounded"
      @input="({ target: { value } }) => emitValue(value)"
    />
  </div>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({
  props: {
    value: {
      type: Number,
      required: true,
    },
  },

  setup(_, { emit }) {
    const emitValue = (input: string) => {
      if (input === '') {
        emit('input', 0)
      } else {
        emit('input', parseInt(input))
      }
    }

    return { emitValue }
  },
})
</script>
