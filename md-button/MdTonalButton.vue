<template>
  <VBtn class="md-tonal-button material-theme" rounded="pill" variant="tonal">
    <slot />
  </VBtn>
</template>

<script lang="ts" setup>
import { VBtn } from 'vuetify/components'
// const props = defineProps({

// })

// const emit = defineEmits({});
</script>

<style lang="scss">
.md-tonal-button {
    background-color: transparent;
    box-shadow: var(--md-sys-color-shadow);
    font-family: var(--md-sys-typescale-label-large-font);
    line-height: var(--md-sys-typescale-label-large-line-height);
    font-size: var(--md-sys-typescale-label-large-size);
    font-weight: var(--md-sys-typescale-label-large-weight);
    color: var(--md-sys-color-on-secondary-container);
    text-transform: none;
    letter-spacing: 0.0125rem;
    height: 40px;
    padding-left: 24px;
    padding-right: 24px;
    > .v-btn__underlay {
      background-color: var(--md-sys-color-secondary-container);
    }
    > .v-btn__content {
        padding: 0;
        display: flex;
        gap: 8px;
        color: inherit;
    }
}
</style>
