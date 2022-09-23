<template>
    <button
        @click="toggleDark()"
        class="switch-theme"
    >{{ isDark ? 'light is off' : 'light is on' }}</button>
</template>

<script setup>
import { useDark, useToggle } from '@vueuse/core'

const isDark = useDark({
    selector: 'html'
})
const toggleDark = useToggle(isDark)
</script>