<template>
  <!-- card unavailable -->
  <div class="unavailable-card">

    <!-- teks utama -->
    <h3>This product is unavailable to show</h3>

    <!-- tombol next -->
    <button class="btn-next" @click="$emit('next')">
      Next product
    </button>

  </div>
</template>

<script>
export default {}; // komponen kosong
</script>
