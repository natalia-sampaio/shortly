<script>
import { useLocalStorage } from '@vueuse/core'

export default {
    data() {
        return {
            links: useLocalStorage("links", []),
            linkWasCopied: null,
        }
    },
    methods: {
        writeToClipboard(text, index) {
            navigator.clipboard
                .writeText(text)
            this.linkWasCopied = index
        }
    }
}
</script>

<template>
    <div>
        <div v-for="(link, index) in links" class="card card--link">
            <span class="original-link">{{ link.originalLink }}</span>
            <div class="card-bottom">
                <span class="short-link">{{ link.shortLink }}</span>
                <button :class="['button', 'button--copy', linkWasCopied==index ? 'button--copied' : '']" @click="() => writeToClipboard(link.shortLink, index)">{{linkWasCopied == index ? 'Copied!' : 'Copy'}}</button>
            </div>
        </div>
    </div>
</template>

<style scoped>
    .button--copied {
        background: var(--very-dark-blue);
    }
    .card--link {
        margin: 1em auto;
        width: 90%;
    }

    .original-link {
        padding: 1em;
        height: 1em;
    }

    .original-link{
        white-space: nowrap;
        overflow: hidden;
        text-overflow: ellipsis;
    }

    .card-bottom {
        border-top: 2px solid var(--very-light-gray);
        padding: 1em;
        display: grid;
    }

    .short-link {
        color: var(--cyan);
        margin-bottom: 1em;
    }

    .button--copy {
        justify-self: center;
        font-family: var(--font);
        font-weight: 700;
        font-size: 16px;
        color: white;
        border-radius: 0.5em;
        width: 100%;
        border: 0;
    }
    
    @media screen and (min-width: 1440px) {
        .card--link {
            width: 1110px;
            display: flex;
            align-items: center;
            justify-content: space-between;
        }

        .original-link {
            width: 50%;
        }

        .card-bottom {
            border: 0;
            width: 50%;
            display: flex;
            align-items: center;
            justify-content: end;
        }

        .short-link {
            margin: 0 1em;
        }

        .button--copy {
            width: 180px;
        }

    }
</style>