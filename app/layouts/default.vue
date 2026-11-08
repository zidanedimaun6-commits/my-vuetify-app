
<script setup lang="ts">
const isLoggedIn = useState('isLoggedIn', () => false)

function logout() {
  isLoggedIn.value = false
  navigateTo('/')
}
</script>

<template>
  <v-app>
    <v-app-bar color="white" elevation="2" class="px-4">
      <v-app-bar-title class="font-weight-bold text-primary">
        Kixk Shop
      </v-app-bar-title>

      <v-spacer></v-spacer>

      <v-btn to="/" variant="text">Home</v-btn>
      <v-btn to="/products" variant="text">Products</v-btn>
      <v-btn to="/about" variant="text">About Us</v-btn>
      <v-btn to="/contactus" variant="text">Contact Us</v-btn>

      <v-btn
        v-if="!isLoggedIn"
        to="/login"
        color="primary"
        variant="flat"
        class="ml-2"
      >
        Login
      </v-btn>

      <v-btn
        v-else
        color="error"
        variant="outlined"
        class="ml-2"
        @click="logout"
      >
        Logout
      </v-btn>
    </v-app-bar>

    <v-main>
      <slot />
    </v-main>
  </v-app>
</template>


<script lang="ts" setup>

</script>

<style>

</style>