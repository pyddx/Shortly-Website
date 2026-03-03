<script setup>
import { ref } from 'vue'

const isOpen = ref(false)

function toggleMenu() {
  isOpen.value = !isOpen.value
}
</script>

<template>
  <nav class="navbar">
    <div class="navbar-inner">

      <div class="logo">Shortly</div>

      <div class="desktop-links">
        <a href="#">Features</a>
        <a href="#">Pricing</a>
        <a href="#">Resources</a>
      </div>

      <div class="desktop-auth">
        <a href="#" class="btn-login">Login</a>
        <a href="#" class="btn-signup">Sign Up</a>
      </div>

      <button class="hamburger" @click="toggleMenu" aria-label="Toggle menu">
        <span v-if="!isOpen">&#9776;</span>
        <span v-else>&#10005;</span>
      </button>

    </div>

    <div v-if="isOpen" class="mobile-menu">
      <a href="#">Features</a>
      <a href="#">Pricing</a>
      <a href="#">Resources</a>
      <hr class="divider" />
      <a href="#">Login</a>
      <a href="#" class="btn-signup-mobile">Sign Up</a>
    </div>
  </nav>
</template>

<style scoped>
.navbar {
  background: white;
  padding: 1.25rem 1.5rem;
}

.navbar-inner {
  max-width: 1100px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  gap: 2rem;
}

.logo {
  font-size: 1.4rem;
  font-weight: 800;
  color: #1e1e47;
}

.desktop-links {
  display: flex;
  gap: 1.75rem;
  margin-right: auto; 
}

.desktop-links a {
  text-decoration: none;
  color: #9e9ea7;
  font-weight: 600;
  font-size: 0.9rem;
  transition: color 0.2s;
}

.desktop-links a:hover {
  color: #1e1e47;
}

.desktop-auth {
  display: flex;
  align-items: center;
  gap: 1.5rem;
}

.btn-login {
  text-decoration: none;
  color: #9e9ea7;
  font-weight: 600;
  font-size: 0.9rem;
  transition: color 0.2s;
}

.btn-login:hover {
  color: #1e1e47;
}

.btn-signup {
  text-decoration: none;
  background: #2acfcf;
  color: white;
  font-weight: 700;
  font-size: 0.9rem;
  padding: 0.55rem 1.4rem;
  border-radius: 50px;
  transition: background 0.2s;
}

.btn-signup:hover {
  background: #1ba8a8;
}

.hamburger {
  display: none; 
  background: none;
  border: none;
  font-size: 1.5rem;
  cursor: pointer;
  color: #1e1e47;
  margin-left: auto;
}

.mobile-menu {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.25rem;
  background: #3a3054;
  padding: 2rem 1.5rem;
  border-radius: 12px;
  margin: 1rem 1.5rem 0;
}

.mobile-menu a {
  text-decoration: none;
  color: white;
  font-weight: 600;
  font-size: 1rem;
}

.divider {
  width: 100%;
  border: none;
  border-top: 1px solid rgba(255, 255, 255, 0.2);
}

.btn-signup-mobile {
  background: #2acfcf;
  color: white !important;
  padding: 0.65rem 2rem;
  border-radius: 50px;
  font-weight: 700;
}

/* ---- breakpoints ---- */

/* Mobile (< 768px): hide desktop nav, show hamburger */
@media (max-width: 767px) {
  .desktop-links,
  .desktop-auth {
    display: none;
  }

  .hamburger {
    display: block;
  }
}

/* Tablet / Desktop (≥ 768px): show desktop nav, hide hamburger */
@media (min-width: 768px) {
  .hamburger {
    display: none;
  }

  .mobile-menu {
    display: none !important;
  }
}
</style>