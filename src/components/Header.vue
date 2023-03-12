<template>
    <header class="header">
        <img src="@/assets/images/logo.svg" alt="Shortly logo" class="header__image">
        <div class="container">
            <input type="checkbox" id="menu" class="container__checkbox">
            <label for="menu" class="container__label">
                <span class="container__image-burger-menu"></span>
            </label>
            <ul class="nav-list">
                <div class="nav-list__top">
                    <li class="nav-list__item">
                        <a href="#" class="link">Features</a>
                    </li>
                    <li class="nav-list__item">
                        <a href="#" class="link">Pricing</a>
                    </li>
                    <li class="nav-list__item">
                        <a href="#" class="link">Resources</a>
                    </li>
                </div>
                <div class="nav-list__bottom">
                    <li class="nav-list__item">
                        <a href="#" class="link">Login</a>
                    </li>
                    <li class="button">
                        <a href="#" class="link link--white">Sign Up</a>
                    </li>
                </div>
            </ul>
        </div>
    </header>
</template>

<style scoped>
.header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 2em 1.5em 1em 1.5em;
}

.container {
    position: relative;
}

.container__checkbox {
    display: none;
}

.container__image-burger-menu {
    width: 64px;
    height: 64px;
    background-image: url("@/assets/images/burger-menu.svg");
    background-repeat: no-repeat;
    background-position: center;
    display: inline-block;
}

.nav-list {
    display: none;
    background: var(--dark-violet);
    border-radius: 0.5em;
    position: absolute;
    top: 100%;
    right: 0;
    width: 76vw;
    padding: 2em 1em;
}

.container__checkbox:checked~.nav-list {
    display: block;
    text-align: center;
}

.nav-list__top {
    border-bottom: 1px solid var(--grayish-violet);
}

.nav-list__item {
    padding: 1em;
}

@media screen and (min-width: 1440px) {
    .header {
        padding: 0;
    }

    .header__image {
        margin-left: 10rem;
    }

    .container__label {
        display: none;
    }

    .nav-list,
    .nav-list__top,
    .nav-list__bottom {
        border-bottom: 0;
        display: flex;
    }

    .nav-list {
        background: white;
        position: relative;
        justify-content: space-between;
    }

    .nav-list__bottom {
        margin-right: 10rem;
    }
}
</style>