<script setup lang="ts">
import { EmptyState } from 'venus';

const primaryButtonData = {
  text: 'add a new one',
  action: () => console.log('adding a new one'),
};

const imageData = {
  url: 'https://i.pinimg.com/originals/dc/da/19/dcda190421b351dd54052996225ca048.png',
  descritiveText: 'snoopy and woodstock relaxing',
  width: '512',
  height: '256',
};

</script>

<template>
  <div class="wrapper">
    <EmptyState 
      header="you're all done!" 
      description="you have done all your labours, enjoy your day 😎"
      :primary-button="primaryButtonData"
      :image="imageData"
    />
  </div>
</template>

<style lang="scss">
.wrapper {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
}
</style>