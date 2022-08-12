<template>
  <p>{{ t('HI') }}</p>
</template>

<script lang="ts" setup>
import { useI18n } from 'vue-i18n'

// const props = defineProps({})

// const emit = defineEmits({})

const { t } = useI18n()
</script>

<style lang="scss" scoped></style>

<i18n locale="en">
{
  "HI": "Hello World"
}
</i18n>

<i18n locale="pl">
{
  "HI": "Witaj świecie"
}
</i18n>

<i18n locale="es">
{
  "HI": "Hola Mundo"
}
</i18n>

