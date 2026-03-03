<script setup lang="ts">
import { ref } from 'vue'
import type { TabItem } from './TabsAccordion.types'

const props = defineProps<{
  items: TabItem[]
  defaultIndex?: number
}>()

const activeIndex = ref<number | null>(0)

function handleToggle(index: number) {
  activeIndex.value =
    activeIndex.value === index ? null : index
}
</script>

<template>
  <div class="tabs">
    <div
      class="tabs__nav"
      role="tablist"
    >
      <button
        v-for="(item, index) in items"
        :key="item.id"
        class="tabs__nav-item"
        :class="{
          'tabs__nav-item--active': activeIndex === index
        }"
        role="tab"
        :aria-selected="activeIndex === index"
        @click="handleToggle(index)"
      >
        {{ item.title }}
      </button>
    </div>

    <div class="tabs__content">
      <div
        v-for="(item, index) in items"
        :key="item.id"
        class="tabs__panel"
        :class="{ 'tabs__panel--active': activeIndex === index }"
      >
        <button
          class="tabs__accordion-trigger"
          :class="{
          'tabs__accordion-trigger--active': activeIndex === index
          }"
          @click="handleToggle(index)"
        >
          {{ item.title }}

          <span
            class="tabs__accordion-icon"
            :class="{
              'tabs__accordion-icon--active': activeIndex === index
            }"
          >
            <span class="tabs__accordion-icon-line tabs__accordion-icon-line--horizontal"></span>
            <span class="tabs__accordion-icon-line tabs__accordion-icon-line--vertical"></span>
          </span> 
        </button>

        <div class="tabs__panel-wrapper">
          <div
            class="tabs__panel-body"
            role="tabpanel"
            v-html="item.content"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped lang="scss">
@use "./TabsAccordion.scss";
</style>