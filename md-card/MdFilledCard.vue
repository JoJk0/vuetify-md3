<template>
  <VCard flat variant="flat" class="md-filled-card" rounded>
    <slot />
  </VCard>
</template>

<script lang="ts" setup>
import { VCard } from 'vuetify/components'
// const props = defineProps({});

// const emit = defineEmits({});
</script>

<style lang="scss" scoped>
.md-filled-card {
    background-color: var(--md-sys-color-surface-variant);
    border-radius: var(--md-sys-shape-corner-medium-default-size);
    box-shadow: none;
}
</style>
