<script setup>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Attribution from './components/Attribution.vue'
import Shorten from './components/Shorten.vue'
import Links from './components/Links.vue';
</script>

<template>
  <Header />
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
  <Shorten />
  <Links />
  <section class="informations">
    <h2 class="informations__title">Advanced Statistics</h2>
    <p class="informations__description">
      Track how your links are performing across the web with our advanced statistics dashboard.
    </p>
    <div class="informations__cards">
      <div class="card">
        <div class="card__image">
          <img src="@/assets/images/icon-brand-recognition.svg" alt="brand recognition">
        </div>
        <h3 class="card__title">Brand Recognition</h3>
        <p class="card__description">
          Boost your brand recognition with each click. Generic links don’t mean a thing. Branded links help instil confidence in your content.
        </p>
        <!-- <hr class="card__strip"> -->
      </div>
      <div class="card">
        <div class="card__image">
          <img src="@/assets/images/icon-detailed-records.svg" alt="detailed records">
        </div>
        <h3 class="card__title">Detailed Records</h3>
        <p class="card__description">
          Gain insights into who is clicking your links. Knowing when and where people engage with your content helps inform better decisions.
        </p>
        <!-- <hr class="card__strip"> -->
      </div>
      <div class="card">
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
  <div class="boost">
    <h2 class="boost__title">Boost your links today</h2>
    <div class="boost__button">
      <div class="button button--get-started">
        <a href="#" class="link link--get-started link--white">Get Started</a>
      </div>
    </div>
  </div>
  <Footer />
  <Attribution />
</template>