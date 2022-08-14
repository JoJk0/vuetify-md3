<template>
  <VBtn :title="title" :to="to" class="md-navigation-bar-item material-theme">
    <VIcon class="icon">
      {{ icon }}
    </VIcon>
    <span class="title">{{ title }}</span>
  </VBtn>
</template>

<script lang="ts" setup>
import type { PropType } from 'vue'
import type { RouteLocationRaw } from 'vue-router'
import { VBtn, VIcon } from 'vuetify/components'

const props = defineProps({
  icon: {
    type: String,
    default: 'mdi-apps',
  },
  title: {
    type: String,
    default: '',
  },
  to: {
    type: Object as PropType<RouteLocationRaw>,
    default: null,
  },
})

// const emit = defineEmits({})
</script>

<style lang="scss">
.md-navigation-bar-item {
  >.v-btn__overlay, >.v-btn__underlay, >.v-ripple__container {
    width: 64px;
    height: 32px;
    border-radius: var(--md-sys-shape-large);
    left: 50%;
    transform: translateX(-50%);
    &.v-btn__overlay, &.v-btn__underlay {
      opacity: 0;
    }
  }

  >.v-btn__content {
    gap: 4px;

    >.icon {
      color: var(--md-sys-color-on-surface-variant);
      width: 64px;
      height: 32px;
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 24px;
    }

    >.title {
      color: var(--md-sys-color-on-surface-variant);
      font-family: var(--md-sys-typescale-label-medium-font);
      line-height: var(--md-sys-typescale-label-medium-line-height);
      font-size: var(--md-sys-typescale-label-medium-size);
      font-weight: var(--md-sys-typescale-label-medium-weight);
      letter-spacing: var(--md-sys-typescale-label-medium-tracking);
    }

  }

  &.v-btn--active {
    > .v-btn__underlay {
        background-color: var(--md-sys-color-secondary-container);
        opacity: var(--md-sys-state-dragged-state-layer-opacity);
    }
    >.v-btn__content {

      >.icon {
        color: var(--md-sys-color-on-secondary-container);
      }

      >.title {
        color: var(--md-sys-color-on-surface);
      }
    }
  }

  &:hover {
    > .v-btn__overlay {
        background-color: var(--md-sys-color-on-surface-variant);
        opacity: var(--md-sys-state-hover-state-layer-opacity);
    }
    >.v-btn__content {
      >.icon {
        color: var(--md-sys-color-on-surface-variant);
      }

      >.title {
        color: var(--md-sys-color-on-surface-variant);
      }
    }

    &.v-btn--active {
      > .v-btn__overlay {
          background-color: var(--md-sys-color-on-surface);
      }
      >.v-btn__content {
        >.icon {
          color: var(--md-sys-color-on-secondary-container);
        }

        >.title {
          color: var(--md-sys-color-on-surface);
        }
      }
    }
  }

  &:active,
  &:focus {
    > .v-btn__overlay {
        background-color: var(--md-sys-color-on-surface-variant);
        opacity: var(--md-sys-state-focus-state-layer-opacity);
    }
    >.v-btn__content {
      >.icon {
        color: var(--md-sys-color-on-surface-variant);
      }

      >.title {
        color: var(--md-sys-color-on-surface-variant);
      }
    }

    &.v-btn--active {
      > .v-btn__overlay {
          background-color: var(--md-sys-color-on-surface);
      }
      >.v-btn__content {
        >.icon {
          color: var(--md-sys-color-on-secondary-container);
        }

        >.title {
          color: var(--md-sys-color-on-surface);
        }
      }
    }
  }
}
</style>
