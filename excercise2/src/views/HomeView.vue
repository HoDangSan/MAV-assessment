<script setup lang="ts">
import type { TabItem } from '@/components/TabsAccordion/TabsAccordion.types';
import TabsAccordion from '@/components/TabsAccordion/TabsAccordion.vue'
import data from '@/data/data.json'

const dataItems = data as TabItem[]
</script>

<template>
  <TabsAccordion
    :items="dataItems"
    :default-index="0"
  />
</template>