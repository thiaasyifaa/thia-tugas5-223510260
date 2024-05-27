<template>
  <div id="app">
    <Navbar />
    <Carousel />

    <div class="product-container">
      <ProductCard
        v-for="product in products"
        :key="product.id"
        :product="product"
        @add-to-cart="handleAddToCart"
      />
    </div>

    <Footer />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue';
import Carousel from './components/Carousel.vue';
import ProductCard from './components/ProductCard.vue';
import Footer from './components/Footer.vue';

export default {
  name: 'App',
  components: {
    Navbar,
    Carousel,
    ProductCard,
    Footer
  },
  data() {
    return {
      products: [
        { id: 1, name: 'TAS', price: 'Rp612.580', imgSrc: 'https://th.bing.com/th?id=OIP.dso62g6VBX2ELuDdCp8E5gHaHa&w=250&h=250&c=8&rs=1&qlt=90&o=6&dpr=1.5&pid=3.1&rm=2 ' },
        { id: 2, name: 'Sneakers', price: 'Rp200.000', imgSrc: 'https://th.bing.com/th?id=OIP.P201e6SNEgV5Ao1wrwiEDgHaHa&w=250&h=250&c=8&rs=1&qlt=90&o=6&dpr=1.5&pid=3.1&rm=2' },
        { id: 3, name: 'Laptop', price: 'Rp300.000', imgSrc: 'https://th.bing.com/th?id=OIP.ycfnnM54CKLO6z4zZRCZzwHaFj&w=288&h=216&c=8&rs=1&qlt=90&o=6&dpr=1.5&pid=3.1&rm=2' }
      ]
    };
  },
  methods: {
    handleAddToCart(product) {
      // Implementasikan logika untuk menambahkan produk ke keranjang
      console.log('Tambah ke keranjang:', product);
    }
  }
}
</script>

<style>
body {
  background-color: #000306;
  margin: 0;
  font-family: Arial, sans-serif;
}

.product-container {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  padding: 20px;
}
</style>