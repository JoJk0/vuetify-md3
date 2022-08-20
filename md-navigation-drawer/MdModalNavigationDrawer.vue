<template>
  <VNavigationDrawer class="md-modal-navigation-drawer material-theme" temporary>
    <div v-if="title || $slots.title" class="md-title">
      {{ title }}
      <slot name="title" />
    </div>
    <slot />
    <template #append>
      <slot name="append" />
    </template>
  </VNavigationDrawer>
</template>

<script lang="ts" setup>
import { VNavigationDrawer } from 'vuetify/components'
const props = defineProps({
  title: {
    type: String,
    default: '',
  },
})

// const emit = defineEmits({});
</script>

<style lang="scss">
.md-modal-navigation-drawer {
    $margin: 12px;
    background-color: var(--md-sys-color-surface);
    color: var(--md-sys-color-on-surface);
    padding: 12px;
    border: 0;
    margin: $margin !important;
    height: calc(100% - $margin * 2) !important;
    border-radius: var(--md-sys-shape-large);
    box-sizing: border-box;

    >.v-navigation-drawer__content,
    >.v-navigation-drawer__append {
        >.md-title {
            color: var(--md-sys-color-on-surface-variant);
            font-family: var(--md-sys-typescale-title-small-font);
            line-height: var(--md-sys-typescale-title-small-line-height);
            font-size: var(--md-sys-typescale-title-small-size);
            font-weight: var(--md-sys-typescale-title-small-weight);
            padding-left: 16px;
            padding-right: 12px;
            display: flex;
            flex-direction: column;
            justify-content: center;
        }

        >.v-list {
            padding: 0;
        }
    }
}
</style>
