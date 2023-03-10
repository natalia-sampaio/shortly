<script>
import { useLocalStorage } from '@vueuse/core'

    export default {
        data() {
        return {
            links: useLocalStorage("links", [])
        }
    }
    }
</script>

<template>
    <div v-for="link in links" class="card__link">
        <span>{{ link.originalLink }}</span>
        <span>{{ link.short_link }}</span>
    </div>
</template>