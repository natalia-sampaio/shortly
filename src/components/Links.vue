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
    <div v-for="link in links" class="card card--link">
        <span class="original-link">{{ link.originalLink }}</span>
        <span class="short-link">{{ link.shortLink }}</span>
        <button class="button button--copy">Copy</button>
    </div>
</template>

<style scoped>
    .card--link {
        margin: 0 auto;
        padding: 0;
        width: 90%;
    }

    .original-link {
        border-bottom: 2px solid var(--very-light-gray);
    }

    .original-link, .short-link {
        padding: 1em;
        height: 1em;
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
    }

    .short-link {
        color: var(--cyan);
    }

    .button--copy {
        font-family: var(--font);
        font-weight: 700;
        font-size: 18px;
        color: white;
        border-radius: 0.5em;
        margin: 0 1em 1em 1em;
        border: 0;
    }
</style>