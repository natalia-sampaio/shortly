<template>
    <div class="boost">
        <h2 class="boost__title">Boost your links today</h2>
        <div class="boost__button">
            <div class="button button--get-started">
                <a href="#" class="link link--get-started link--white">Get Started</a>
            </div>
        </div>
    </div>
</template>

<style scoped>
.boost {
    background: url("@/assets/images/bg-boost-mobile.svg") no-repeat;
    background-size: cover;
    background-color: var(--very-dark-blue);
    height: 300px;
    display: grid;
    align-items: center;
    justify-content: center;
}

.boost__title {
    font-size: 30px;
    font-weight: 700;
    color: white;
    align-self: end;
}

.boost__button {
    justify-self: center;
}

@media screen and (min-width: 1440px) {
    .boost {
        background: url("@/assets/images/bg-boost-desktop.svg") no-repeat;
        background-size: cover;
        background-color: var(--very-dark-blue);
        height: 250px;
    }

    .boost__title {
        font-size: 36px;
    }
}
</style>