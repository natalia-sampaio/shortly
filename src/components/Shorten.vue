<script>
import { useLocalStorage } from '@vueuse/core'

export default {
    data() {
        return {
            url: "",
            links: useLocalStorage("links", []),
            error: false,
        }
    },
    methods: {
        async shorten() {
            this.error = false;
            if (this.url === "") {
                this.error = true;
                return;
            }
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
            return response.result.full_short_link
        }
    }
}
</script>

<template>
    <div class="shorten">
        <div class="shorten-form">
            <div class="shorten-form__box">
                <input v-model="url" type="url" placeholder="Shorten a link here..." aria-label="input for url to be shortened"
                :class="['shorten-form__input', error ? 'error-input' :'']">
                <span v-if="error" class="error-message">Please add a link</span>
            </div>
            <button type="button" class="button button--shorten-form" @click.prevent="shorten">
                <span class="link link--white">Shorten It!</span>
            </button>
        </div>
    </div>
</template>

<style scoped>
.shorten {
    margin: 8em 0 -3em 0;
}

.shorten-form {
    background: url("@/assets/images/bg-shorten-mobile.svg") no-repeat;
    background-position-x: right;
    background-position-y: top;
    background-color: var(--very-dark-violet);
    display: grid;
    align-items: center;
    border-radius: 0.5em;
    width: 350px;
    height: 160px;
    position: relative;
    top: -80px; /* because this is half of the form height */
    margin: 0 auto;
}

.shorten-form__box {
    text-align: center;
}

.shorten-form__input {
    width: 80%;
    border-radius: 0.5em;
    border: 0;
    padding: 1.2em;
}

.shorten-form__input::placeholder {
    font: var(--font);
    font-size: 18px;
    font-weight: 500;
}

.error-message {
    font-size: 16px;
    color: red;
    font-style: italic;
    margin: 0 auto;
    display: block;
}
.error-input {
    border: 1px solid red;
}
.error-input::placeholder {
    background: red;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
    text-decoration: none;
}

@media screen and (min-width: 1440px) {
    .shorten-form {
        background: url("@/assets/images/bg-shorten-desktop.svg") no-repeat;
        background-position-x: right;
        background-position-y: top;
        background-color: var(--very-dark-violet);
        width: 1110px;
        display: flex;
        flex-wrap: wrap;
    }

    .shorten-form__box {
        width: 80%;
    }

    .shorten-form__input {
        border-radius: 0.5em;
        border: 0;
        padding: 1.2em;
    }
}
</style>