<script setup>
import logo from './assets/images/svgs/logo-dark.svg'
import greenMangoShake from './assets/images/green-mango-shake-dark.jpg'
import sisig from './assets/images/sisig.webp'
import porkSinigang from './assets/images/pork-sinigang.jpg'
import freshSpringRoll from './assets/images/fresh-spring-roll.jpg'
import pancit from './assets/images/pancit.webp'
import adobo from './assets/images/adobo.jpg'
import pandanCake from './assets/images/pandan-cake.jpg'
import casavaCake from './assets/images/casava-cake.webp'
import tocino from './assets/images/tocino.webp'
import facebookLogo from './assets/images/facebook.png'
import instagramLogo from './assets/images/instagram.png'
import xLogo from './assets/images/X.png'
import tiktokLogo from './assets/images/tiktok.png'

import CardComponent from './components/CardComponent.vue'

</script>

<template>
  <header class="header-section">
    <a href="/" class="header-logo">
      <img class="header-logo-image" :src="logo" alt="Sarap Cookbook Logo" />
      <span class="header-title hide-on-mobile">Sarap Cookbook</span>
    </a>
    <nav>
      <ul class="header-nav-items">
        <li><a class="btn header-nav-buttons" href="/">Home</a></li>
        <li><a class="btn header-nav-buttons" href="">Recipes</a></li>
      </ul>
    </nav>
  </header>

  <main>
    <section class="hero-section">
      <div class="hero-content-greet">
        <h1 class="hero-title">
          Make your favorite <span class="hero-highlight-word">Filipino Dishes</span> with
          <p>Sarap Cookbook</p>
        </h1>
        <p class="hero-paragraph">
          The ultimate accessible guide to make your favorite filipino dish.
        </p>
      </div>
      <div class="hero-carousel"></div>
    </section>
    <section class="categories-section">
      <h2 class="categories-section-title">Categories</h2>
      <div class="categories-section-items">
        <CardComponent
          name="Green Mango Shake"
          :image="greenMangoShake"
          imageAlt="Photo of Green Mango Shake"
          category="Inumin"
          link="/inumin"
        />
        <CardComponent
          name="Sisig"
          :image="sisig"
          imageAlt="Photo of Sisig dish"
          category="Pampagana"
          link="/pampagana"
        />
        <CardComponent
          name="Pork Sinigang"
          :image="porkSinigang"
          imageAlt="Photo of Pork Sinigang dish"
          category="Sabaw"
          link="/sabaw"
        />
        <CardComponent
          name="Fresh Spring Roll"
          :image="freshSpringRoll"
          imageAlt="Photo of Fresh Spring Roll dish"
          category="Gulay"
          link="/gulay"
        />
        <CardComponent
          name="Pancit"
          :image="pancit"
          imageAlt="Photo of Pancit dish"
          category="Luto sa Bigas at Pancit"
          link="/luto-sa-bigas-at-pancit"
        />
        <CardComponent
          name="Adobo"
          :image="adobo"
          imageAlt="Photo of Adobo dish"
          category="Ulam"
          link="/ulam"
        />
        <CardComponent
          name="Pandan Cake"
          :image="pandanCake"
          imageAlt="Photo of Pandan Cake"
          category="Panghimagas"
          link="/panghimagas"
        />
        <CardComponent
          name="Casava Cake"
          :image="casavaCake"
          imageAlt="Photo of Casava Cake"
          category="Kakanin"
          link="/kakanin"
        />

        <CardComponent
          name="Tocino"
          :image="tocino"
          imageAlt="Photo of Tocino"
          category="Pag-iimbak ng Pagkain"
          link="/pag-iimbak-ng-pagkain"
        />
      </div>
    </section>
    <section class="footer-section">
      <img class="footer-section-logo" :src="logo" alt="Logo of the Sarap Cookbook" />
      <div class="footer-section-socials">
        <p class="footer-section-social-title">Follow Us</p>
        <div class="footer-section-socials-icons">
          <a href="https://facebook.com">
            <img class="footer-section-socials-icon" :src="facebookLogo" alt="Logo of Facebook" />
          </a>
          <a href="instagram.com">
            <img class="footer-section-socials-icon" :src="instagramLogo" alt="Logo of Instagram" />
          </a>
          <a href="x.com">
            <img class="footer-section-socials-icon" :src="xLogo" alt="Logo of X" />
          </a>
          <a href="tiktok.com">
            <img class="footer-section-socials-icon" :src="tiktokLogo" alt="Logo of Tiktok" />
          </a>
        </div>
      </div>
      <p class="footer-copyright">&copy; All Rights Reserved</p>
    </section>
  </main>
</template>

<style scoped>
.header-section {
  display: flex;
  justify-content: space-between;
  padding: 2.5rem;
  align-items: center;
  min-height: var(--header-height);
}

.header-logo {
  display: flex;
  align-items: center;
  gap: 1rem;
}

.header-logo-image {
  width: 5rem;
}

.header-title {
  font-size: 1.953rem;
  font-weight: var(--font-weight-bold);
}

.header-nav-items {
  display: flex;
  flex-direction: row;
  gap: 2rem;
  font-size: 1rem;
  letter-spacing: var(--letter-spacing-wide);
}

.header-nav-buttons {
  background-color: var(--color-primary-light);
  font-size: 1rem;
  font-family: 'Poppins', 'Roboto', 'Playfair Display', sans-serif;
  display: inline-block;
  padding: .8rem 2rem;
  border-radius: .4rem;
}

.header-nav-buttons:hover {
  background-color: var(--color-primary-dark);
  color: var(--color-white);
}

.header-nav-sidebar {
  display: none;
}

.hero-section {
  height: calc(70vh - var(--header-height));
  margin-bottom: 10rem;
  display: flex;
  align-items: center;
  width: 100%;
}

.hero-content-greet {
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 100%;
  width: 100%;
  margin-left: 4rem;
}

.hero-title {
  font-size: 3.815rem;
  margin-bottom: 1rem;
  line-height: 1.3;
}

.hero-highlight-word {
  color: var(--color-primary-light);
  display: inline-block;
}

.hero-paragraph {
  font-size: 1.2rem;
  font-family: 'Roboto', 'Poppins', 'Playfair Display', sans-serif;
  letter-spacing: 1px;
}

.hero-carousel {
  margin: 0 5rem;
  width: 75vw;
  max-width: 100%;
  box-shadow: 20px 20px 10px gray;
  aspect-ratio: 1/.7;
  background-size: 100% 100%;
  border-radius: 2rem;
  animation: slider 10s ease infinite;
}

@keyframes slider {
  0% {
    background-image: url(./assets/images/adobo.jpg);
  }

  30% {
    background-image: url(./assets/images/casava-cake.webp);
  }

  60% {
    background-image: url(./assets/images/sisig.webp);
  }

  80% {
    background-image: url(./assets/images/tocino.webp);
  }

  100% {
    background-image: url(./assets/images/pancit.webp);
  }
}

.categories-section {
  margin-bottom: 20rem;
  height: auto;
}

.categories-section-title {
  font-size: 3.052rem;
  font-weight: var(--font-weight-bold);
  text-align: center;
  margin-bottom: 2rem;

}

.categories-section-items {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
  margin: 0 10%;
  width: 80%;
  height: 100%;
}

.footer-section {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
}

.footer-section-logo {
  margin-bottom: 4rem;
}

.footer-section-socials {
  display: flex;
  flex-direction: column;
  align-content: center;
  margin-bottom: 4rem;
}

.footer-section-social-title {
  font-size: 1.953rem;
  margin-bottom: 1rem;
}

.footer-section-socials-icons {
  display: flex;
  gap: 1rem;
}

.footer-section-socials-icon {
  width: 2rem;
}

.footer-copyright {
  font-size: 0.8rem;
}

/* 2xl */
@media (max-width: 1536px) {
  .header-nav-buttons {
    padding: .5rem 1rem;
  }

  .hero-content-greet {
    margin-left: 3rem;
  }

  .hero-title {
    font-size: calc(1rem + 2.9vw);
    margin-bottom: .5rem;
  }

  .hero-carousel {
    margin-left: 3rem;
    margin-right: 1rem;
  }

  .categories-section-title {
    font-size: calc(1rem + 3vw);
  }
}

/* xl */
@media (max-width: 1280px) {
  .header-title {
    font-size: 1.563rem;
  }

  .header-nav-buttons {
    padding: .5rem 1rem;
  }

  .hero-content-greet {
    margin-left: 1%;
  }

  .hero-title {
    font-size: calc(1rem + 2.8vw);
    margin-bottom: 10px;
  }

  .hero-paragraph {
    font-size: 1rem;
  }

  .hero-carousel {
    margin: 0 1rem;
    max-width: 75vw;
  }
}

/* lg */
@media (max-width: 1024px) {
  .header-section {
    padding: 2rem 1rem 0 1rem;
    margin-bottom: 2rem;
  }

  .header-title {
    font-size: calc(1rem + .5vw);
  }

  .header-nav-buttons {
    padding: .5rem 1rem;
  }

  .hero-content-greet {
    margin-left: 1rem;
  }

  .hero-title {
    font-size: calc(1rem + 2.5vw);
    margin-bottom: .1rem;
  }

  .hero-paragraph {
    font-size: 0.8rem;
  }

  .hero-carousel {
    margin: 0 1rem 0 2rem;
    width: 80vw;
  }
  .categories-section-items {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* md */
@media (max-width: 768px) {
  .header-section {
    padding: 1.5rem;
    margin-bottom: 4rem;
  }

  .header-logo-image {
    width: 4rem;
  }


  .header-nav-items {
    gap: 1.5rem;
  }

  .header-nav-buttons {
    padding: .3rem .8rem;
  }

  .hero-section {
    flex-direction: column;
    margin-bottom: 20vh;
  }

  .hero-content-greet {
    text-align: center;
    margin: 0 1rem 4rem 1rem;
    height: 30%;
    padding: 0 3rem
  }

  .hero-title {
    font-size: calc(1rem + 3.9vw);
    margin-bottom: .5rem;
  }

  .hero-carousel {
    width: 60vw;
    margin: 0;
  }
  .categories-section-items {
    grid-template-columns: repeat(2, 1fr);
  }
}

/* sm */
@media (max-width: 640px) {
  .header-section {
    padding: 1.5rem;
    margin-bottom: 3rem;
  }

  .header-title{
    display: none;
  }

  .header-nav-items {
    gap: 1rem;
  }

  .header-nav-buttons {
    padding: .4rem .4rem;
  }

  .hero-section {
    padding: 0 1rem;
    margin-bottom: 20vh;
  }

  .hero-content-greet {
    padding: 0;
    margin-bottom: 3rem;
  }

  .hero-title {
    font-size: calc(1rem + 3.5vw);
    margin-bottom: .5rem;
  }

  .hero-paragraph {
    font-size: 1rem;
  }

  .categories-section-items {
    grid-template-columns: repeat(1, 1fr);
  }
}

/* xs */
@media (max-width: 475px) {
  .hide-on-mobile {
    display: none;
  }

  .header-section {
    margin-bottom: 2rem;
    padding: 1.5rem .5rem;
  }

  .header-logo-image {
    width: 3rem;
  }

  .header-nav-items {
    gap: .3rem;
    font-size: 0.8rem;
  }

  .hero-section {
    margin-bottom: 20vh;
  }

  .hero-content-greet {
    margin-bottom: 3rem;
  }

  .hero-title {
    font-size: calc(1rem + 3.5vw);
    width: 100%;
  }

  .hero-paragraph {
    font-size: 0.8rem;
  }

  .hero-carousel {
    width: 100vw;
  }

  .categories-section-items {
    grid-template-columns: repeat(1, 1fr);
  }
}
</style>
