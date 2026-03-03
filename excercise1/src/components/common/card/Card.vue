<script setup lang="ts">
import type { Feature } from '../../../types/feature';
import BaseButton from '../base-button/BaseButton.vue'

defineProps<{
    feature: Feature
}>()    
</script>

<template>
  <div class="card p-6">
    <div class="card__wrapper-image">
      <img
        class="card__img"
        :src="feature.image"
        alt="Card thumbnail"
      />
    </div>

    <div class="card__body mt-6">
      <p class="card__text">
        {{ feature.description }}
      </p>

      
    </div>

    <div class="card__footer mt-6">
        <BaseButton class="">READ MORE</BaseButton>
    </div>
  </div>
</template>

<style lang="scss" scoped>
@use "./Card.scss";
</style>