<script>
import { useLocalStorage } from '@vueuse/core'

export default {
    data() {
        return {
            url: "",
            links: useLocalStorage("links", [])
        }
    },
    methods: {
        async shorten() {
            const shortLink = await this.getShortenedLink()
            const link = {
                "shortLink": shortLink,
                "originalLink": this.url
            }

            this.links.push(link)
            this.url = ""
        },
        async getShortenedLink() {
            const request = `https://api.shrtco.de/v2/shorten?url=${this.url}`;
            const fetchResponse = await fetch(request);
            const response = await fetchResponse.json();
            return response.result.short_link
        }
    }
}
</script>

<template>
    <div class="shorten-form">
        <input v-model="url" type="url" placeholder="Shorten a link here..." aria-label="input for url to be shortened"
        class="shorten-form__input">
        <button type="button" class="button button--shorten-form" @click.prevent="shorten">
            <span class="link link--white">Shorten It!</span>
        </button>
    </div>
</template>