
<script setup lang="ts">
const socials = [
  {
    name: 'Facebook',
    icon: 'mdi-facebook',
    color: '#1877F2',
    link: 'https://www.facebook.com/',
  },
  {
    name: 'Instagram',
    icon: 'mdi-instagram',
    color: '#E4405F',
    link: 'https://www.instagram.com/',
  },
  {
    name: 'TikTok',
    icon: 'mdi-music-note',
    color: '#000000',
    link: 'https://www.tiktok.com/',
  },
]
</script>

<template>
  <v-container class="py-12">
    <div class="text-center mb-10">
      <h1 class="text-h4 font-weight-bold mb-3">Contact Us</h1>
      <p class="text-grey-darken-1">
        Have questions? Connect with us through our social media accounts.
      </p>
    </div>

    <v-card
      max-width="650"
      class="mx-auto pa-6"
      rounded="xl"
      elevation="2"
    >
      <h2 class="text-h6 font-weight-bold text-center mb-6">
        Follow Kixk Shop
      </h2>

      <v-row justify="center">
        <v-col
          v-for="social in socials"
          :key="social.name"
          cols="4"
          class="text-center"
        >
          <v-btn
            :href="social.link"
            target="_blank"
            :color="social.color"
            icon
            size="x-large"
            variant="flat"
          >
            <v-icon size="32">{{ social.icon }}</v-icon>
          </v-btn>

          <p class="mt-3 font-weight-medium">
            {{ social.name }}
          </p>
        </v-col>
      </v-row>
    </v-card>
  </v-container>
</template>

<script lang="ts" setup>

</script>

<style>

</style>