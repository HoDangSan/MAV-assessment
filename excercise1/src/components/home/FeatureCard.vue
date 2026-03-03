<script setup lang="ts">
import Card from '../common/card/Card.vue'
import type { Feature } from '../../types/feature';

defineProps<{
  feature: Feature
}>()
</script>

<template>
  <Card
    :key="feature.id"
    :feature="feature"
  />
</template>