<script setup>
</script>

<template>
  <section class="cta">
    <div class="cta-inner">
      <h2>Boost your links today</h2>
      <a href="#" class="btn-get-started">Get Started</a>
    </div>
  </section>
</template>

<style scoped>
.cta {
  background-color: #3a3054;
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;

  padding: 5rem 1.5rem;
  text-align: center; 
}

.cta-inner {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2rem;
}

.cta-inner h2 {
  color: white;
  font-size: clamp(1.4rem, 4vw, 2.25rem);
  font-weight: 900;
  margin: 0;
}

.btn-get-started {
  display: inline-block;
  background: #2acfcf;
  color: white;
  font-weight: 700;
  font-size: 1rem;
  padding: 0.85rem 2.5rem;
  border-radius: 50px;
  text-decoration: none;
  transition: background 0.2s;
}

.btn-get-started:hover {
  background: #1ba8a8;
}
</style>