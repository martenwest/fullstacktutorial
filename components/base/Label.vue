<template>
  <label class="flex flex-col w-full max-w-md cursor-pointer">
    <span class="w-32 font-medium leading-none text-gray-800">
      {{ label }}
    </span>

    <p class="text-sm text-gray-700">{{ message }}</p>

    <div class="flex-1 w-full mt-2">
      <slot />
    </div>
  </label>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({
  props: {
    label: {
      type: String,
      required: true,
    },
    message: {
      type: String,
      required: true,
    },
  },
})
</script>
