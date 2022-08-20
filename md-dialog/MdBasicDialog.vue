<template>
  <VDialog class="md-basic-dialog material-theme">
    <template #activator>
      <slot name="activator" />
    </template>
    <VCard class="card">
      <slot />
    </VCard>
  </VDialog>
</template>

<script lang="ts" setup>
import { VCard, VDialog } from 'vuetify/components'
// const props = defineProps({})

// const emit = defineEmits({})
</script>

<style lang="scss" scoped>
.md-basic-dialog {
    .card {
        background-color: var(--md-sys-color-surface);
        box-shadow: var(--md-sys-elevation-level3);
        color: var(--md-sys-color-on-surface-variant);
        border-radius: var(--md-sys-shape-corner-extra-large-default-size);
    }
}
</style>
