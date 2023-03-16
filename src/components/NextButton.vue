<script setup lang="ts">
import { Random, dayNo } from '~/state'
import { t } from '~/i18n'

function next() {
  const day = Random(1, 1509)
  dayNo.value = day
}
</script>

<template>
  <button
    btn flex="~ wrap gap-x-2 center" ws-nowrap text-lg font-serif
    p="x3 y1"
    @click="next()"
  >
    {{ t('next-start') }}
  </button>
</template>
