<template>
    <header class="header">
        <img src="@/assets/images/logo.svg" alt="Shortly logo" class="header__image">
        <div class="container">
            <input type="checkbox" id="menu" class="container__checkbox">
            <label for="menu" class="container__label">
                <span class="container__image-burger-menu"></span>
            </label>
            <ul class="nav-list">
                <div class="nav-list__part-1">
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
                <div class="nav-list__part-2">
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