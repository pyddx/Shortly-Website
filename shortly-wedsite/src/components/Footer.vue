<script setup>
</script>

<template>
  <footer class="footer">
    <div class="footer-inner">
      <div class="footer-logo">Shortly</div>

      <nav class="footer-nav">
        <div class="footer-col">
          <h4>Features</h4>
          <a href="#">Link Shortening</a>
          <a href="#">Branded Links</a>
          <a href="#">Analytics</a>
        </div>

        <div class="footer-col">
          <h4>Resources</h4>
          <a href="#">Blog</a>
          <a href="#">Developers</a>
          <a href="#">Support</a>
        </div>

        <div class="footer-col">
          <h4>Company</h4>
          <a href="#">About</a>
          <a href="#">Our Team</a>
          <a href="#">Careers</a>
          <a href="#">Contact</a>
        </div>
      </nav>

      <!-- Social icons -->
      <div class="footer-social">
        <a href="#" aria-label="Facebook">
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" viewBox="0 0 24 24">
            <path d="M18 2h-3a5 5 0 00-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 011-1h3z"/>
          </svg>
        </a>

        <a href="#" aria-label="Twitter">
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" viewBox="0 0 24 24">
            <path d="M23 3a10.9 10.9 0 01-3.14 1.53 4.48 4.48 0 00-7.86 3v1A10.66 10.66 0 013 4s-4 9 5 13a11.64 11.64 0 01-7 2c9 5 20 0 20-11.5a4.5 4.5 0 00-.08-.83A7.72 7.72 0 0023 3z"/>
          </svg>
        </a>

        <a href="#" aria-label="Pinterest">
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="currentColor" viewBox="0 0 24 24">
            <path d="M12 2C6.48 2 2 6.48 2 12c0 4.24 2.65 7.86 6.39 9.29-.09-.78-.17-1.98.04-2.83.18-.77 1.23-5.22 1.23-5.22s-.31-.63-.31-1.56c0-1.46.85-2.55 1.9-2.55.9 0 1.33.67 1.33 1.48 0 .9-.57 2.26-.87 3.52-.25 1.05.52 1.9 1.55 1.9 1.86 0 3.12-2.4 3.12-5.23 0-2.16-1.46-3.68-3.55-3.68-2.42 0-3.84 1.82-3.84 3.7 0 .73.28 1.52.63 1.94.07.08.08.16.06.24-.06.27-.2.85-.23.97-.04.16-.13.19-.3.12-1.12-.52-1.82-2.16-1.82-3.47 0-2.82 2.05-5.4 5.91-5.4 3.1 0 5.51 2.21 5.51 5.17 0 3.08-1.94 5.56-4.63 5.56-.9 0-1.75-.47-2.04-1.02l-.56 2.06c-.2.77-.74 1.73-1.11 2.32.84.26 1.72.4 2.64.4 5.52 0 10-4.48 10-10S17.52 2 12 2z"/>
          </svg>
        </a>

        <a href="#" aria-label="Instagram">
          <svg xmlns="http://www.w3.org/2000/svg" width="20" height="20" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round" viewBox="0 0 24 24">
            <rect x="2" y="2" width="20" height="20" rx="5" ry="5"/>
            <circle cx="12" cy="12" r="4"/>
            <line x1="17.5" y1="6.5" x2="17.51" y2="6.5"/>
          </svg>
        </a>
      </div>

    </div>
  </footer>
</template>

<style scoped>
.footer {
  background: #232127;
  padding: 3rem 1.5rem;
}

.footer-inner {
  max-width: 1100px;
  margin: 0 auto;
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2.5rem;
  text-align: center;
}

.footer-logo {
  font-size: 1.5rem;
  font-weight: 900;
  color: white;
}

.footer-nav {
  display: flex;
  flex-direction: column; 
  gap: 2rem;
  align-items: center;
}

.footer-col {
  display: flex;
  flex-direction: column;
  gap: 0.6rem;
  align-items: center; 
}

.footer-col h4 {
  color: white;
  font-size: 0.9rem;
  font-weight: 700;
  margin: 0 0 0.4rem;
}

.footer-col a {
  text-decoration: none;
  color: #9e9ea7;
  font-size: 0.9rem;
  transition: color 0.2s;
}

.footer-col a:hover {
  color: #2acfcf;
}

.footer-social {
  display: flex;
  gap: 1.25rem;
  align-items: center;
}

.footer-social a {
  color: white;
  display: flex;
  transition: color 0.2s;
}

.footer-social a:hover {
  color: #2acfcf;
}

@media (min-width: 1024px) {
  .footer-inner {
    flex-direction: row;   
    align-items: flex-start;
    text-align: left;
    justify-content: space-between;
  }

  .footer-nav {
    flex-direction: row;      
    gap: 4rem;
    align-items: flex-start;
  }

  .footer-col {
    align-items: flex-start;  
  }

}
</style>