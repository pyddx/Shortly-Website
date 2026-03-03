<script setup>
import { ref } from 'vue'

const inputUrl  = ref('')
const errorMsg  = ref('')

const links = ref([
  { original: 'https://frontendmentor.io',          short: 'https://rel.ink/k4lKyk', copied: false },
  { original: 'https://twitter.com/frontendmentor', short: 'https://rel.ink/gx0Xp9', copied: false },
  { original: 'https://linkedin.com/frontend-mentor',short: 'https://rel.ink/gob3X9', copied: false },
])

function shortenLink() {
  if (!inputUrl.value.trim()) {
    errorMsg.value = 'Please add a link'
    return
  }

  errorMsg.value = ''

  const chars = 'abcdefghijklmnopqrstuvwxyz0123456789'
  const code  = Array.from({ length: 6 }, () => chars[Math.floor(Math.random() * chars.length)]).join('')

  links.value.unshift({
    original: inputUrl.value,
    short: `https://rel.ink/${code}`,
    copied: false,
  })

  inputUrl.value = ''
}

function copyLink(index) {
  navigator.clipboard.writeText(links.value[index].short).catch(() => {})
  links.value[index].copied = true
  setTimeout(() => { links.value[index].copied = false }, 2000)
}
</script>

<template>
  <section class="shorten">
    <div class="shorten-inner">

      <div class="shorten-card">
        <div class="form-row">

          <div class="input-wrap">
            <input
              v-model="inputUrl"
              type="url"
              placeholder="Shorten a link here..."
              :class="['link-input', { 'link-input--error': errorMsg }]"
              @keyup.enter="shortenLink"
            />
            <span v-if="errorMsg" class="error-text">{{ errorMsg }}</span>
          </div>

          <button class="btn-shorten" @click="shortenLink">Shorten It!</button>

        </div>
      </div>

      <div class="results">
        <div v-for="(link, i) in links" :key="i" class="result-card">

          <span class="original-url">{{ link.original }}</span>

          <div class="result-right">
            <a :href="link.short" class="short-url">{{ link.short }}</a>
            <button
              class="btn-copy"
              :class="{ 'btn-copy--copied': link.copied }"
              @click="copyLink(i)"
            >
              {{ link.copied ? 'Copied!' : 'Copy' }}
            </button>
          </div>

        </div>
      </div>

    </div>
  </section>
</template>

<style scoped>
.shorten {
  background: #f0f1f6;
  padding: 0 0 4rem;
}

.shorten-inner {
  max-width: 900px;
  margin: 0 auto;
  padding: 0 1.5rem;
  transform: translateY(-3rem); 
}

.shorten-card {
  background: #090c34;
  border-radius: 12px;
  padding: 1.75rem 1.5rem;
  margin-bottom: 1.5rem;
}

.form-row {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.input-wrap {
  position: relative;
  display: flex;
  flex-direction: column;
  flex: 1;
}

.link-input {
    background: white;
  padding: 0.85rem 1.25rem;
  border-radius: 8px;
  border: 3px solid transparent;
  font-size: 1rem;
  outline: none;
  transition: border-color 0.2s;
}

.link-input::placeholder { color: #bfbfbf; }
.link-input:focus        { border-color: #2acfcf; }
.link-input--error       { border-color: #f46262 !important; }

.error-text {
  color: #f46262;
  font-size: 0.8rem;
  font-style: italic;
  margin-top: 4px;
}

.btn-shorten {
  background: #2acfcf;
  color: white;
  font-weight: 700;
  font-size: 1rem;
  padding: 0.85rem 2rem;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  transition: background 0.2s;
}

.btn-shorten:hover { background: #1ba8a8; }

.results {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.result-card {
  background: white;
  border-radius: 8px;
  padding: 1rem 1.25rem;

  display: flex;
  flex-direction: column;
  gap: 0.75rem;
}

.original-url {
  color: #1e1e47;
  font-size: 0.9rem;
  word-break: break-all;
}

.result-right {
  display: flex;
  flex-direction: column;
  gap: 0.6rem;
}

.short-url {
  color: #2acfcf;
  font-size: 0.9rem;
  text-decoration: none;
}

.short-url:hover { text-decoration: underline; }

.btn-copy {
  background: #2acfcf;
  color: white;
  font-weight: 700;
  font-size: 0.85rem;
  padding: 0.55rem 1.5rem;
  border: none;
  border-radius: 6px;
  cursor: pointer;
  transition: background 0.2s;
}

.btn-copy:hover         { background: #1ba8a8; }
.btn-copy--copied       { background: #3a3054; }

/* ---- Tablet / Desktop (≥ 768px): switch to row layout ---- */
@media (min-width: 768px) {
  .form-row {
    flex-direction: row;
    align-items: flex-start;
  }

  .btn-shorten {
    white-space: nowrap;
  }

  .result-card {
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
    gap: 1rem;
  }

  .original-url {
    flex: 1;
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
  }

  .result-right {
    flex-direction: row;
    align-items: center;
    flex-shrink: 0;
  }
}
</style>