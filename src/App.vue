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

import { ref } from 'vue'

const showSidebar = ref(false)

const toggleSidebar = () => {
  showSidebar.value = !showSidebar.value
  console.log(showSidebar.value)
}
</script>

<template>
  <header class="header-section">
    <div class="header-logo-container">
      <img class="header-logo-image" :src="logo" alt="Sarap Cookbook Logo" />
      <p class="header-title hide-on-mobile">Sarap Cookbook</p>
    </div>
    <nav class="hide-on-mobile">
      <ul class="header-nav-items">
        <li><a class="btn header-nav-buttons" href="/">Home</a></li>
        <li><a class="btn header-nav-buttons" href="">Recipes</a></li>
      </ul>
    </nav>
    <nav class="header-nav-sidebar" ref="sidebar">
      <a @click="toggleSidebar">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          height="40px"
          viewBox="0 -960 960 960"
          width="40px"
          fill="#b39a81"
          v-if="showSidebar"
        >
          <path
            d="m251.33-204.67-46.66-46.66L433.33-480 204.67-708.67l46.66-46.66L480-526.67l228.67-228.66 46.66 46.66L526.67-480l228.66 228.67-46.66 46.66L480-433.33 251.33-204.67Z"
          />
        </svg>
        <svg
          xmlns="http://www.w3.org/2000/svg"
          height="40px"
          viewBox="0 -960 960 960"
          width="40px"
          fill="#b39a81"
          v-else
        >
          <path
            d="M120-240v-66.67h720V-240H120Zm0-206.67v-66.66h720v66.66H120Zm0-206.66V-720h720v66.67H120Z"
          />
        </svg>
      </a>
      <ul class="header-nav-items-sidebar">
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
      <h3 class="categories-section-title">Categories</h3>
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

<style scoped></style>
