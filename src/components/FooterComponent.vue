<script setup>
import logo from '../assets/images/svgs/logo-dark.svg'
import facebookLogo from '../assets/images/facebook.png'
import instagramLogo from '../assets/images/instagram.png'
import xLogo from '../assets/images/X.png'
import tiktokLogo from '../assets/images/tiktok.png'
</script>

<template>
  <footer class="footer-section">
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
  </footer>
</template>

<style scoped>
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
</style>
