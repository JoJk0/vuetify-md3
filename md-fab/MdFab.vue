<template>
  <VBtn class="md-fab">
    <slot />
  </VBtn>
</template>

<script lang="ts" setup>
import { VBtn } from 'vuetify/components'
// const props = defineProps({})

// const emit = defineEmits({})
</script>

<style lang="scss" scoped>
.md-fab {
    position: fixed;
    bottom: 2em;
    right: 2em;
    text-transform: none;
    background-color: var(--md-sys-color-primary-container);
    box-shadow: var(--md-sys-elevation-level3);
    color: var(--md-sys-color-on-primary-container);
    font-family: var(--md-sys-typescale-button-font);
    line-height: var(--md-sys-typescale-button-line-height);
    font-size: var(--md-sys-typescale-button-size);
    letter-spacing: var(--md-sys-typescale-button-tracking);
    font-weight: var(--md-sys-typescale-button-weight);
    &:hover {
        box-shadow: var(--md-sys-elevation-level4);
    }
    &:active, &:focus {
        box-shadow: var(--md-sys-elevation-level3);
    }
    min-width: 56px;
    height: 56px;
    border-radius: var(--md-sys-shape-large);
    padding: 16px;
}
</style>
