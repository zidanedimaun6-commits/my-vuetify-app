
<script setup lang="ts">

const PRODUCTS = [
  {
    name: "Nike Pegasus",
    price: "₱5,495",
    description: "Comfortable running shoes with maximum cushioning.",
    src: "/images/nike.jpg",
  },
  {
    name: "Kobe A.D. Protro Men's Basketball Shoes",
    price: "₱8,595",
    description: "Responsive running shoes with a primeknit upper.",
    src: "/images/adidas.jpg",
  },
  {
    name: "Dunk Low Retro",
    price: "₱6,295",
    description: "Classic lifestyle sneakers.",
    src: "/images/puma.jpg",
  },
  {
    name: "Jordan Strada Men's Basketball Shoes",
    price: "₱6,995",
    description: "Classic lifestyle sneakers.",
    src: "/images/puma.jpg",
  },
  {
    name: "Classic Evo Gum Unisex Cloge",
    price: "₱4,200",
    description: "Classic lifestyle sneakers.",
    src: "/images/puma.jpg",
  },
  {
    name: "Air Jordan 1 Mid SE Men's Basketball Shoes",
    price: "₱7,995",
    description: "Classic lifestyle sneakers.",
    src: "/images/puma.jpg",
  }
]

</script>

<template>
 

    <v-container class="py-8">

    <!-- Welcome Section -->
    <v-sheet
      color="grey-lighten-4"
      rounded="lg"
      class="pa-8 mb-10 text-center"
    >
      <h1 class="text-h3 font-weight-bold mb-3">
        Welcome to Kixk Shop
      </h1>

      <p class="text-body-1 text-grey-darken-1 mb-5">
        Find your perfect shoes for sports and everyday activities.
      </p>

      <v-btn
        color="primary"
        to="/products"
        size="large"
      >
        Explore Products
      </v-btn>
    </v-sheet>

    <!-- Products Section -->
    <div class="mb-6">
      <h2 class="text-h4 font-weight-bold">
        Featured Products
      </h2>

      <p class="text-grey mt-2">
        Discover our latest shoe collection.
      </p>
    </div>

    <v-row>

      <v-col
        v-for="product in PRODUCTS"
        :key="product.name"
        cols="12"
        sm="6"
        md="4"
      >
        <v-card class="pa-4" elevation="2">

          <v-img
            :src="product.src"
            height="200"
            cover
            class="bg-grey-lighten-2 rounded mb-4"
          ></v-img>

          <v-card-title class="px-0 pt-0">
            {{ product.name }}
          </v-card-title>

          <v-card-text class="px-0 pb-0">

            <p class="text-body-1 mb-3">
              {{ product.description }}
            </p>

            <p class="text-subtitle-1 font-weight-bold text-primary">
              {{ product.price }}
            </p>

          </v-card-text>

        </v-card>
      </v-col>

    </v-row>

  </v-container>
</template>


<script lang="ts" setup>

</script>

<style>

</style>