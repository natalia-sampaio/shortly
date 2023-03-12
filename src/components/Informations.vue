<template>
    <section class="informations">
        <h2 class="informations__title">Advanced Statistics</h2>
        <p class="informations__description">
            Track how your links are performing across the web with our advanced statistics dashboard.
        </p>
        <div class="informations__cards">
            <div class="card card--informations">
                <div class="card__image">
                    <img src="@/assets/images/icon-brand-recognition.svg" alt="brand recognition">
                </div>
                <h3 class="card__title">Brand Recognition</h3>
                <p class="card__description">
                    Boost your brand recognition with each click. Generic links don’t mean a thing. Branded links help instil confidence in your content.
                </p>
                <!-- <hr class="card__strip"> -->
            </div>
            <div class="card card--informations">
                <div class="card__image">
                    <img src="@/assets/images/icon-detailed-records.svg" alt="detailed records">
                </div>
                <h3 class="card__title">Detailed Records</h3>
                <p class="card__description">
                    Gain insights into who is clicking your links. Knowing when and where people engage with your content helps inform better decisions.
                </p>
                <!-- <hr class="card__strip"> -->
            </div>
            <div class="card card--informations">
                <div class="card__image">
                    <img src="@/assets/images/icon-fully-customizable.svg" alt="fully customizable">
                </div>
                <h3 class="card__title">Fully Customizable</h3>
                <p class="card__description">
                    Improve brand awareness and content discoverability through customizable links, supercharging audience engagement.
                </p>
            </div>
        </div>
    </section>
</template>

<style>
.informations {
    margin-top: 5em;
    text-align: center;
}

.informations__title {
    font-size: 30px;
    font-weight: 700;
    color: var(--very-dark-blue);
}

.informations__description {
    color: var(--grayish-violet);
    line-height: 1.6em;
    margin: 2em 1em 6em 1em;
}

.informations {
    padding-bottom: 6em;
    margin-bottom: -6em;
}

@media screen and (min-width: 1440px) {
    .informations__title,
    .informations__description {
        max-width: 40%;
    }

    .informations__title {
        margin: 0 auto;
    }

    .informations__description {
        margin: 1em auto;
    }

    .informations__cards {
        display: flex;
        justify-content: space-between;
        margin: 6em 10rem;
    }
}
</style>