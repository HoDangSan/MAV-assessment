<script setup lang="ts">
import FeatureCard from './FeatureCard.vue'
import { features } from '@/data/features';
</script>

<template>
  <section class="features">
    <FeatureCard
      v-for="feature in features"
      :key="feature.id"
      :feature="feature"
    />
  </section>
</template>

<style scoped>
.features {
  display: flex;
  flex-wrap: wrap;
  gap: 48px;
  padding: 48px 24px;
  justify-content: center;
  background: #ffffff;
}
</style>