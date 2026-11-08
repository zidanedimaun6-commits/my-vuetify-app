
<script setup lang="ts">
import { ref } from 'vue'

const isLoggedIn = useState('isLoggedIn', () => false)

const email = ref('')
const password = ref('')

function login() {
  if (!email.value || !password.value) {
    return
  }

  isLoggedIn.value = true

  navigateTo('/')
}
</script>

<template>
  <v-container class="py-12">

    <v-card
      max-width="400"
      class="mx-auto pa-6"
      elevation="2"
    >

      <h2 class="text-h5 font-weight-bold text-center mb-6">
        Login to Kixk Shop
      </h2>

      <v-text-field
        v-model="email"
        label="Email"
        prepend-inner-icon="mdi-email"
        variant="outlined"
      ></v-text-field>

      <v-text-field
        v-model="password"
        label="Password"
        prepend-inner-icon="mdi-lock"
        type="password"
        variant="outlined"
      ></v-text-field>

      <v-btn
        color="primary"
        block
        size="large"
        @click="login"
      >
        Sign In
      </v-btn>

      <p class="text-caption text-grey text-center mt-4">
        Welcome to Kixk Shop!
      </p>

    </v-card>

  </v-container>
</template>

<style scoped>
</style>


<script lang="ts" setup>

</script>

<style>

</style>