<template>
    <div class="card">
      <img :src="product.imgSrc" class="card-img" :alt="product.name">
      <div class="card-body">
        <h5 class="card-title">{{ product.name }}</h5>
        <p class="card-text">{{ product.price }}</p>
        <button @click="$emit('add-to-cart', product)" class="btn">Tambah ke Keranjang</button>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      product: Object
    }
  }
  </script>
  
  <style scoped>
  .card {
    border: 1px solid #ddd;
    border-radius: 5px;
    overflow: hidden;
    margin: 20px;
    width: 300px;
  }
  
  .card-img {
    width: 100%;
    height: auto;
  }
  
  .card-body {
    padding: 15px;
  }
  
  .card-title {
    font-size: 1.25rem;
    margin-bottom: 10px;
  }
  
  .card-text {
    font-size: 1rem;
    margin-bottom: 15px;
  }
  
  .btn {
    background-color: #007bff;
    color: white;
    border: none;
    padding: 10px 15px;
    cursor: pointer;
  }
  
  .btn:hover {
    background-color: #73b0f1;
  }
  </style>