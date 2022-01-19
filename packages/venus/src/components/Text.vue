<template>
  <span :class="size"><slot /></span>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'

export default defineComponent({
  props: {
    size: {
      required: true,
      type: Object as PropType<'large' | 'normal'>,
    }
  }
})
</script>

<style lang="scss" scoped>
span {
  color: #080808;
  font-size: 16px;
}

.large {
  font-size: 36px;
}

.normal {
  font-size: 20px;
}
</style>
