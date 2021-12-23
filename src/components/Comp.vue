<template>
  <div>
     <slot/>
  </div>
</template>

<script lang="ts">
import type { PropType } from 'vue'
import { defineComponent } from 'vue'

export default defineComponent({
  props: {
    submit: {
      type: Function as PropType<() => boolean>,
      required: true
    }
  },
  emits: {
    reset: () => true,
  }
})
</script>
