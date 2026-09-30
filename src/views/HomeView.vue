<script setup lang="ts">
import LinkButton from '@/components/LinkButton.vue'

const links = [
  { label: 'Portfolio', url: 'https://pollyzebrowski.com', icon: 'mdi-earth' },
  {
    label: 'LinkedIn',
    url: 'https://www.linkedin.com/in/polly-zebrowski',
    icon: 'mdi-linkedin',
  },
  { label: 'Email', url: 'mailto:hello@pollyzebrowski.com', icon: 'mdi-email' },
]
</script>

<template>
  <v-app>
    <v-main class="d-flex align-center justify-center bg-grey-lighten-5">
      <v-container class="d-flex align-center justify-center py-8">
        <v-row justify="center" class="ma-0 fill-width">
          <v-col cols="12" sm="8" md="6" lg="4" class="d-flex justify-center">
            <v-card
              class="pa-6 text-center rounded-xl elevation-6 profile-card"
              color="transparent"
              variant="flat"
              style="background: linear-gradient(135deg, rgba(255,255,255,0.95), rgba(224,231,255,0.92)); border: 1px solid rgba(147, 197, 253, 0.45); width: 100%; max-width: 480px;"
            >
              <div class="d-flex justify-center">
                <v-avatar size="108" color="indigo-lighten-5" class="avatar-wrap mb-5">
                  <span class="text-h5 font-weight-bold text-indigo-darken-3">PZ</span>
                </v-avatar>
              </div>

              <p class="text-uppercase text-caption text-medium-emphasis mb-2">
                Designer • Developer • Creator
              </p>
              <h1 class="text-h3 font-weight-bold mb-2">Polly Zebrowski</h1>
              <p class="text-body-1 text-medium-emphasis mb-6">
                I build thoughtful digital experiences and turn bold ideas into simple, beautiful
                products.
              </p>

              <div class="d-flex flex-column ga-3 link-stack">
                <LinkButton
                  v-for="link in links"
                  :key="link.label"
                  :label="link.label"
                  :url="link.url"
                  :icon="link.icon"
                />
              </div>
            </v-card>
          </v-col>
        </v-row>
      </v-container>
    </v-main>
  </v-app>
</template>
