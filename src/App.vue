<template>
  <!-- wrapper halaman -->
  <div class="page-wrapper" :class="pageClass">

    <!-- produk tersedia -->
    <ProductCard
      v-if="product"
      :product="product"
      @next="nextProduct"
    />

    <!-- produk tidak ada -->
    <UnavailableProduct
      v-else
      @next="nextProduct"
    />

  </div>
</template>

<script>
import ProductCard from './components/ProductCard.vue';
import UnavailableProduct from './components/UnavailableProduct.vue';

export default {
  components: { 
    ProductCard, 
    UnavailableProduct 
  },

  data() {
    return {
      index: 1,   // ID produk
      product: null // data produk
    };
  },

  methods: {
    // ambil produk berikutnya
    async nextProduct() {
      const res = await fetch(`https://fakestoreapi.com/products/${this.index}`);
      const data = await res.json();

      // hanya terima kategori pakaian
      if (data.category === "men's clothing" || data.category === "women's clothing") {
        this.product = data;
      } else {
        this.product = null;
      }

      // loop dari 1 → 20 → balik lagi
      this.index = this.index === 20 ? 1 : this.index + 1;
    }
  },

  computed: {
    // ubah background sesuai kategori
    pageClass() {
      if (!this.product) return "unavailable";
      if (this.product.category === "men's clothing") return "men";
      if (this.product.category === "women's clothing") return "women";
      return "unavailable";
    }
  },
  
  mounted() {
    this.nextProduct(); // load awal
  }
};
</script>

<style>
@import "./assets/style.css";
</style>
