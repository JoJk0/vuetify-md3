<template>
  <VCardTitle class="md-card-title material-theme">
    <slot />
  </VCardTitle>
</template>

<script lang="ts" setup>
import { VCardTitle } from 'vuetify/components'
// const props = defineProps({})

// const emit = defineEmits({})
</script>

<style lang="scss" scoped>
.md-card-title {
    color: var(--md-sys-color-on-surface);
    font-family: var(--md-sys-typescale-headline-small-font);
    line-height: var(--md-sys-typescale-headline-small-line-height);
    font-size: var(--md-sys-typescale-headline-small-size);
    font-weight: var(--md-sys-typescale-headline-small-weight);
    letter-spacing: var(--md-sys-typescale-headline-small-tracking);
}
</style>
