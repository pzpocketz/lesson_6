<script setup lang="ts">
const links = [
  { label: 'Portfolio', href: 'https://pollyzebrowski.com' },
  { label: 'LinkedIn', href: 'https://www.linkedin.com/in/polly-zebrowski' },
  { label: 'Email', href: 'mailto:hello@pollyzebrowski.com' },
]
</script>

<template>
  <main class="page-shell">
    <section class="profile-card" aria-label="Polly Zebrowski profile card">
      <div class="avatar" aria-label="Profile photo placeholder">PZ</div>

      <p class="eyebrow">Designer • Developer • Creator</p>
      <h1>Polly Zebrowski</h1>
      <p class="tagline">
        I build thoughtful digital experiences and turn bold ideas into simple, beautiful
        products.
      </p>

      <nav class="link-list" aria-label="Main links">
        <a
          v-for="link in links"
          :key="link.label"
          :href="link.href"
          class="link-button"
          target="_blank"
          rel="noreferrer noopener"
        >
          {{ link.label }}
        </a>
      </nav>
    </section>
  </main>
</template>
