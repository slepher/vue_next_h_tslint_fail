<script lang="ts">
import { defineComponent, h, PropType } from 'vue'

import TestComponent from './Comp.vue'

export default defineComponent({
  props: {
    submit: {
      type: Function as PropType<() => boolean>
    }
  },
  setup(props, { slots }) {
    return () => {
      return h(TestComponent, {}, () =>
        slots.default ? slots.default() : undefined
      )
    }
  }
})
</script>
