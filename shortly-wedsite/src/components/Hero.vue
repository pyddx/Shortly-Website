<script setup>
</script>

<template>
  <section class="hero">
    <div class="hero-inner">
      <div class="hero-image">
        <img src="/images/illustration-working.svg" alt="Person with link illustration" />
      </div>

      <!-- Text block -->
      <div class="hero-text">
        <h1>Turn every link into a brand touchpoint</h1>
        <p>Boost trust with branded links—and see exactly how every link performs.</p>
        <a href="#" class="btn-get-started">Get Started</a>
      </div>

    </div>
  </section>
</template>

<style scoped>
.hero {
  background: white;
  padding: 3rem 1.5rem 4rem;
  overflow: hidden;
}

.hero-inner {
  max-width: 1100px;
  margin: 0 auto;
  display: flex;

  flex-direction: column-reverse;
  align-items: center;
  gap: 2rem;

  text-align: center; 
}

/* ---- image ---- */
.hero-image {
  width: 100%;
  max-width: 380px;
}

.hero-image img {
  width: 100%;
  display: block;
}

.hero-text {
  display: flex;
  flex-direction: column;
  align-items: center; 
}

.hero-text h1 {
  font-size: clamp(1.75rem, 5vw, 3rem);
  font-weight: 900;
  color: #1e1e47;
  line-height: 1.15;
  margin: 0 0 1rem;
}

.hero-text p {
  color: #9e9ea7;
  font-size: 1rem;
  line-height: 1.7;
  margin: 0 0 2rem;
  max-width: 360px;
}

/* ---- CTA button ---- */
.btn-get-started {
  display: inline-block;
  background: #2acfcf;
  color: white;
  font-weight: 700;
  font-size: 0.95rem;
  padding: 0.8rem 2.25rem;
  border-radius: 50px;
  text-decoration: none;
  transition: background 0.2s;
}

.btn-get-started:hover {
  background: #1ba8a8;
}

/* ---- Desktop (≥ 1024px): two-column layout ---- */
@media (min-width: 1024px) {
  .hero-inner {
    flex-direction: row;       
    text-align: left;
    align-items: center;
    justify-content: space-between;
  }

  .hero-text {
    align-items: flex-start;   
    max-width: 480px;
  }

  .hero-image {
    max-width: 45%;
  }
}
</style>