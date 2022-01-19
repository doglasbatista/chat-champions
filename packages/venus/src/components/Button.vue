<template>
  <button :class="hierarchy"><slot /></button>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'

export default defineComponent({
  name: 'Button',
  props: {
    hierarchy: {
      required: false,
      type: Object as PropType<'primary' | 'secondary'>,
      default: 'primary',
    }
  }
})
</script>

<style lang="scss" scoped>
button {
  padding: 8px 16px;
  border: navajowhite;
  box-sizing: border-box;
  border-radius: 3px;
  cursor: pointer;
  transition: .3s ease-in;

  &:hover {
    transition: .3s ease-in;
    background-color: lighten(#080808, 10%);
  }
}

.primary {
  background-color: #080808;
  color: #FFF;

  &:hover {
    transition: .3s ease-in;
    background-color: lighten(#080808, 10%);
  }
}

.secondary {
  border: 1px solid #080808;
  color:  #080808;
  background-color: #fff;

  &:hover {
    transition: .3s ease-in;
    background-color: darken(#fff, 10%);
  }
}
</style>
