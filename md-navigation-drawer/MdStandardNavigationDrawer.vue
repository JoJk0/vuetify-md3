<template>
  <v-navigation-drawer class="md-standard-navigation-drawer material-theme" permanent>
    <div v-if="title" class="md-title">
      {{ title }}
    </div>
    <slot />
    <template #append>
      <slot name="append" />
    </template>
  </v-navigation-drawer>
</template>

<script lang="ts" setup>
const props = defineProps({
  title: {
    type: String,
    default: '',

  },
})

// const emit = defineEmits({});
</script>

<style lang="scss">
.md-standard-navigation-drawer {
    background-color: var(--md-sys-color-surface);
    color: var(--md-sys-color-on-surface);
    padding: 12px;
    border: 0;
    > .v-navigation-drawer__content {
        > .md-title {
            color: var(--md-sys-color-on-surface-variant);
            font-family: var(--md-sys-typescale-title-small-font);
            line-height: var(--md-sys-typescale-title-small-line-height);
            font-size: var(--md-sys-typescale-title-small-size);
            font-weight: var(--md-sys-typescale-title-small-weight);
                height: 56px !important;
                    padding-left: 16px;
                    padding-right: 12px;
                    display: flex;
                    flex-direction: column;
                    justify-content: center;
        }
        > .v-list {
            padding: 0;
        }
    }
}
</style>
