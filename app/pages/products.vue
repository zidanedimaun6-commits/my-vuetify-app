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
    name: "Jordan Strada Men's Basketball Shoes  ",
    price: "₱6,995",
    description: "Classic lifestyle sneakers.",
    src: "/images/puma.jpg",
  },
  {
    name: "Classic Evo Gum Unisex Cloge",
    price: "₱4,200",
    description: "Classic lifestyle sneakers.",
    src: "/images/puma.jpg",
  }
]
</script>

<template> 
<v-btn to="/" variant="text">
    Home
  </v-btn>
  <div>
    <h1>Product List</h1>
    <v-row>
      
      <v-col v-for="product in PRODUCTS" :key="product.name" cols="12" md="4">
        <v-card class="pa-4">
          
         
          <v-img
            :src="product.src"
            height="200px"
            cover
            class="bg-grey-lighten-2 rounded mb-4"
          ></v-img>

          <v-card-title class="px-0 pt-0">{{ product.name }}</v-card-title>
          
          <v-card-text class="px-0 pb-0">
            <p class="text-body-1 mb-2">{{ product.description }}</p>
            <p class="text-subtitle-1 font-weight-bold text-primary">{{ product.price }}</p>
          </v-card-text>

        </v-card>
      </v-col>
    </v-row>
  </div>
</template>

<style scoped>
/* Optional styling */
</style>
