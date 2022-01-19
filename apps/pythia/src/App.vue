<script setup lang="ts">
import { EmptyState } from 'venus';

const primaryButtonData = {
  text: 'fix the query',
  action: () => console.log('fixing the query'),
};

const secondaryButtonData = {
  text: 'never mind',
  action: () => console.log('cacelling'),
}

const imageData = {
  url: 'https://st4.depositphotos.com/4177785/29441/v/380/depositphotos_294418314-stock-illustration-tarot-cards-linear-icon-thin.jpg?forcejpeg=true',
  descritiveText: 'snoopy and woodstock relaxing',
  width: '380',
  height: '380',
};

</script>

<template>
  <div class="wrapper">
    <EmptyState
      header="no results found" 
      description="try adjusting your query to find you're looking for."
      :primary-button="primaryButtonData"
      :secondary-button="secondaryButtonData"
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
