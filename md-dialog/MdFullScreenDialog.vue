<template>
  <VDialog class="md-full-screen-dialog material-theme" fullscreen transition="scroll-y-transition" :scrim="false">
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
.md-full-screen-dialog {
}
    .card {
        background-color: var(--md-sys-color-surface);
        box-shadow: var(--md-sys-elevation-level3);
        color: var(--md-sys-color-on-surface-variant);
        border-radius: 0;
    }
</style>
