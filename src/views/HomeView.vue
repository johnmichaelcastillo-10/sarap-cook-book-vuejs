<script setup>
import greenMangoShake from '../assets/images/green-mango-shake-dark.jpg'
import sisig from '../assets/images/sisig.webp'
import porkSinigang from '../assets/images/pork-sinigang.jpg'
import freshSpringRoll from '../assets/images/fresh-spring-roll.jpg'
import pancit from '../assets/images/pancit.webp'
import adobo from '../assets/images/adobo.jpg'
import pandanCake from '../assets/images/pandan-cake.jpg'
import casavaCake from '../assets/images/casava-cake.webp'
import tocino from '../assets/images/tocino.webp'

import CardComponent from '../components/CardComponent.vue'
</script>

<template>
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
</template>

<style scoped>
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
  aspect-ratio: 1/0.7;
  background-size: 100% 100%;
  border-radius: 2rem;
  animation: slider 10s ease infinite;
}

@keyframes slider {
  0% {
    background-image: url(../assets/images/adobo.jpg);
  }

  30% {
    background-image: url(../assets/images/casava-cake.webp);
  }

  60% {
    background-image: url(../assets/images/sisig.webp);
  }

  80% {
    background-image: url(../assets/images/tocino.webp);
  }

  100% {
    background-image: url(../assets/images/pancit.webp);
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

/* 2xl */
@media (max-width: 1536px) {
  .hero-content-greet {
    margin-left: 3rem;
  }

  .hero-title {
    font-size: calc(1rem + 2.9vw);
    margin-bottom: 0.5rem;
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
  .hero-content-greet {
    margin-left: 1rem;
  }

  .hero-title {
    font-size: calc(1rem + 2.5vw);
    margin-bottom: 0.1rem;
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
  .hero-section {
    flex-direction: column;
    margin-bottom: 20vh;
  }

  .hero-content-greet {
    text-align: center;
    margin: 0 1rem 4rem 1rem;
    height: 30%;
    padding: 0 3rem;
  }

  .hero-title {
    font-size: calc(1rem + 3.9vw);
    margin-bottom: 0.5rem;
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
    margin-bottom: 0.5rem;
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
