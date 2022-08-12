<template>
  <VListItem
    class="md-navigation-drawer-item material-theme" :prepend-icon="prependIcon"
    :append-icon="appendIcon" :title="title" :active="active" rounded="pill" :value="value" :to="to"
  />
</template>

<script lang="ts" setup>
import { VListItem } from 'vuetify/components'
// const props = defineProps<typeof VListItem['']>()
const props = defineProps({
  prependIcon: {
    type: String,
    default: '',
  },
  appendIcon: {
    type: String,
    default: '',

  },
  title: {
    type: String,
    default: '',
  },
  value: {
    type: String,
    default: '',
  },
  active: {
    type: Boolean,
    default: false,
  },
  to: {
    type: Object,
    default: undefined,
  },
})

// const emit = defineEmits({});
</script>

<style lang="scss">
.md-navigation-drawer-item {
    color: var(--md-sys-color-on-surface-variant);
    font-family: var(--md-sys-typescale-label-large-font);
    line-height: var(--md-sys-typescale-label-large-line-height);
    font-size: var(--md-sys-typescale-label-large-size);
    font-weight: var(--md-sys-typescale-label-large-weight);
    height: 56px !important;
    padding-left: 16px;
    padding-right: 12px;
    display: flex;
    gap: 12px;
    background-color: transparent;
    >.v-list-item__overlay {}

    >.v-list-item__content {}

    >.v-list-item__prepend > * {
        color: inherit;
        opacity: 1;
        margin: 0;
    }

    >.v-list-item__append {
        margin-right: 12px;
    }

    &.v-list-item--active {
        >.v-list-item__overlay {
            background-color: var(--md-sys-color-secondary-container);
        }

        >.v-list-item__content,
        >.v-list-item__prepend,
        >.v-list-item__append {
            color: var(--md-sys-color-on-secondary-container);
        }
    }

    &:hover {
        >.v-list-item__overlay {
            background-color: var(--md-sys-color-on-surface);
            opacity: var(--md-sys-state-hover-state-layer-opacity);
        }

        >.v-list-item__content,
        >.v-list-item__prepend,
        >.v-list-item__append {
            color: var(--md-sys-color-on-surface);
        }

        &.v-list-item--active {
            >.v-list-item__overlay {
                background-color: var(--md-sys-color-on-secondary-container);
            }

            >.v-list-item__content,
            >.v-list-item__prepend,
            >.v-list-item__append {
                color: var(--md-sys-color-on-secondary-container);
            }
        }
    }

    &:active,
    &:focus {
        >.v-list-item__overlay {
            background-color: var(--md-sys-color-on-surface);
            opacity: var(--md-sys-state-focus-state-layer-opacity);
        }

        >.v-list-item__content,
        >.v-list-item__prepend,
        >.v-list-item__append {
            color: var(--md-sys-color-on-surface);
        }

        &.v-list-item--active {
            >.v-list-item__overlay {
                background-color: var(--md-sys-color-on-secondary-container);
            }

            >.v-list-item__content,
            >.v-list-item__prepend,
            >.v-list-item__append {
                color: var(--md-sys-color-on-secondary-container);
            }
        }
    }
}
</style>
