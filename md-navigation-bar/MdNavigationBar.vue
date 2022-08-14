<template>
  <VBottomNavigation hide-on-scroll class="md-navigation-bar material-theme">
    <slot />
  </VBottomNavigation>
</template>

<script lang="ts" setup>
import { VBottomNavigation } from 'vuetify/components'
// const props = defineProps({})

// const emit = defineEmits({})
</script>

<style lang="scss" scoped>
.md-navigation-bar {
    background-color: var(--md-sys-color-surface);
    box-shadow: var(--md-sys-elevation-level2);
    height: 80px !important;
    padding-top: 12px;
    padding-bottom: 16px;
}
</style>
