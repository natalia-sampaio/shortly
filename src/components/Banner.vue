<template>
    <section class="banner">
        <img src="@/assets/images/illustration-working.svg" alt="illustration of a person working" class="banner__image">
        <div class="banner__content">
            <h1 class="banner__title">More than just shorter links</h1>
            <p class="banner__description">Build your brand’s recognition and get detailed insights on how your links are performing.</p>
            <div class="button button--get-started">
                <a href="#" class="link link--get-started link--white">Get Started</a>
            </div>
        </div>
    </section>
</template>

<style scoped>
.banner {
    text-align: center;
    padding: 1em 1.5em;
}

.banner__image {
    margin-bottom: 2em;
    width: 130vw;
}

.banner__content {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
}

.banner__title {
    font-size: 36px;
    font-weight: 700;
    color: var(--very-dark-blue);
}

.banner__description {
    color: var(--grayish-violet);
    margin: 1em 0;
    line-height: 1.6em;
}

@media screen and (min-width: 1440px) {
    .banner {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        padding: 0;
    }

    .banner__image {
        width: auto;
        grid-column: 3 / 5;
        margin-left: 5em;
    }

    .banner__content {
        display: grid;
        justify-content: left;
        text-align: left;
        grid-column: 1 / 3;
        grid-row: 1 / 2;
        margin: 5rem 0 0 10rem;
    }

    .banner__image {
        grid-row: 1 / 3;
    }

    .banner__title {
        font-size: 70px;
    }

}
</style>