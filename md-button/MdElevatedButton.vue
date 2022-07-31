<template>
    <v-btn class="md-button">
        <slot></slot>
    </v-btn>
</template>

<script lang="ts" setup>

export type MdButtonVariant = 'elevated' | 'filled' | 'tonal' | 'outlined' | 'text';

const props = defineProps({
    variant: {
        type: String,
        default: 'elevated',
    },
});

// const emit = defineEmits({});


</script>

<style lang="scss" scoped>
</style>