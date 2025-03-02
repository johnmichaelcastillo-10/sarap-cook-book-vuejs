<script setup>
import logo from '../assets/images/svgs/logo-dark.svg'
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

/* 2xl */
@media (max-width: 1536px) {
  .header-nav-buttons {
    padding: .5rem 1rem;
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
}
</style>
