<template>
    <footer class="footer">
        <div class="footer__image">
            <img src="@/assets/images/logo-footer.svg" alt="Shortly logo">
        </div>
        <ul class="footer__list">
            <li class="footer__list-title">Features</li>
            <li class="footer__list-item">
                <a href="#" class="footer__link">Link Shortening</a>
            </li>
            <li class="footer__list-item">
                <a href="#" class="footer__link">Branded Links</a>
            </li>
            <li class="footer__list-item">
                <a href="#" class="footer__link">Analytics</a>
            </li>
        </ul>
        <ul class="footer__list">
            <li class="footer__list-title">Resources</li>
            <li class="footer__list-item">
                <a href="#" class="footer__link">Blog</a>
            </li>
            <li class="footer__list-item">
                <a href="#" class="footer__link">Developers</a>
            </li>
            <li class="footer__list-item">
                <a href="#" class="footer__link">Support</a>
            </li>
        </ul>
        <ul class="footer__list">
            <li class="footer__list-title">Company</li>
            <li class="footer__list-item">
                <a href="#" class="footer__link">About</a>
            </li>
            <li class="footer__list-item">
                <a href="#" class="footer__link">Our Team</a>
            </li>
            <li class="footer__list-item">
                <a href="#" class="footer__link">Careers</a>
            </li>
            <li class="footer__list-item">
                <a href="#" class="footer__link">Contact</a>
            </li>
        </ul>
        <ul class="footer__list footer__list-contact">
            <li class="footer__list-item">
                <a href="#" class="footer__link"><img src="@/assets/images/icon-facebook.svg" alt="icon facebook"></a>
            </li>
            <li class="footer__list-item">
                <a href="#" class="footer__link"><img src="@/assets/images/icon-twitter.svg" alt="icon twitter"></a>
            </li>
            <li class="footer__list-item">
                <a href="#" class="footer__link"><img src="@/assets/images/icon-pinterest.svg" alt="icon pinterest"></a>
            </li>
            <li class="footer__list-item">
                <a href="#" class="footer__link"><img src="@/assets/images/icon-instagram.svg" alt="icon instagram"></a>
            </li>
        </ul>
    </footer>
</template>

<style scoped>
.footer {
    background: var(--very-dark-violet);
    padding: 3em 4em;
    text-align: center;
}

.footer__list {
    text-align: center;
    margin-top: 3em;
}

.footer__list-title {
    color: white;
    margin-bottom: 2em;
}

.footer__list-item {
    margin-bottom: 1em;
}

.footer__link {
    text-decoration: none;
    color: var(--grayish-violet);
}

.footer__list-contact {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
    margin-top: 3em;
}

@media screen and (min-width: 1440px) {
    .footer {
        display: grid;
        grid-template-columns: 2fr repeat(4, 1fr);
        padding: 3em 10rem;
    }

    .footer__image {
        grid-column: 1 / 2;
        justify-self: left;
    }

    .footer__list {
        margin-top: 0;
        text-align: left;
    }

    .footer__list-contact {
        grid-column: -1 / -2;
        margin: 0;
    }
}
</style>