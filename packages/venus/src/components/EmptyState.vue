<template>
  <div class="empty-state">
    <img
      v-if="image"
      :src="image.url" 
      :alt="image.descritiveText"
      :width="image.width"
      :height="image.height"
    />
    <Text size="large">{{ header }}</Text>
    <Text size="normal" v-if="description">
      {{ description }}
    </Text>
    <div class="actions" v-if="primaryButton || secondaryButton">
      <Button
        v-if="secondaryButton"
        hierarchy="secondary"
        @click="secondaryButton.action"
      >
        {{ secondaryButton.text }}
      </Button>
      <Button v-if="primaryButton" @click="primaryButton.action">
        {{ primaryButton.text }}
      </Button>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineComponent, PropType } from 'vue'

import Button from './Button.vue';
import Text from './Text.vue';

type ActionButtonProps = {
  text: string;
  action:() => void;
};

type ImageProps = {
  url: string;
  descritiveText: string;
  width: string;
  height: string;
};

defineProps<{
  header: string;
  description?: string;
  primaryButton?: ActionButtonProps;
  secondaryButton?: ActionButtonProps;
  image?: ImageProps;
}>()

</script>

<style lang="scss" scoped>
.empty-state {
  display: flex;
  flex-direction: column;
  align-items: center;
}

img {
  margin-bottom: 16px;
}

.actions {
  margin-top: 16px;
  display: flex;
  column-gap: 8px;
}

</style>
