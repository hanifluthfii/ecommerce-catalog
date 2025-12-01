<template>
  <!-- card produk -->
  <div class="product-card">

    <!-- gambar kiri -->
    <img :src="product.image" alt="Product Image" />

    <!-- info kanan -->
    <div class="product-info">

      <!-- judul -->
      <h2 class="product-title">{{ product.title }}</h2>

      <!-- kategori + rating -->
      <div class="info-row">
        <p class="product-category">{{ product.category }}</p>

        <div class="rating">
          <span class="rate-number">{{ product.rating.rate }}/5</span>

          <!-- bulatan rating -->
          <div class="bullets">
            <span
              v-for="n in 5"
              :key="n"
              class="bullet"
              :class="{ off: n > Math.round(product.rating.rate) }"
            ></span>
          </div>
        </div>
      </div>

      <!-- garis ungu -->
      <div class="top-divider"></div>

      <!-- deskripsi -->
      <p class="product-description">
        {{ product.description }}
      </p>

      <!-- garis abu -->
      <div class="divider"></div>

      <!-- harga -->
      <p class="product-price">${{ product.price }}</p>

      <!-- tombol -->
      <div class="actions">
        <button class="btn-buy">Buy now</button>
        <button class="btn-next" @click="$emit('next')">Next product</button>
      </div>

    </div>
  </div>
</template>

<script>
export default {
  props: ["product"], // data produk
};
</script>
