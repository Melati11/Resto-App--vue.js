<template>
  <div>
    <div class="row">
      <div class="col-span-12">
        <img src="@/assets/detail_spotlight.jpg" alt="" class="w-100" />
      </div>
    </div>
    <div class="container">
      <div class="row mt-3">
        <div class="scrolling-wrapper d-flex">
          <div class="col-span-4 me-2">
            <img src="@/assets/gbr1.jpg" alt="" />
          </div>
          <div class="col-span-4 me-2">
            <img src="@/assets/gbr2.jpg" alt="" />
          </div>
          <div class="col-span-4 me-2">
            <img src="@/assets/gbr3.jpg" alt="" />
          </div>
          <div class="col-span-4 me-2">
            <img src="@/assets/gbr1.jpg" alt="" />
          </div>
          <div class="col-span-4 me-2">
            <img src="@/assets/gbr2.jpg" alt="" />
          </div>
          <div class="col-span-4 me-2">
            <img src="@/assets/gbr3.jpg" alt="" />
          </div>
        </div>
      </div>
      <div class="product-title mt-5">
        <h1>{{ data.name }}</h1>
        <button class="category mt-1">Company Profile Website</button>
        <h3 class="pricey mt-3">Rp. {{ data.price }}</h3>
        <p class="text-secondary">Stock : {{ data.stock }}</p>
      </div>
      <div class="dec mt-5 mb-3">
        <h1 class="mb-4">Tentang Produk</h1>
        <span class="fs-6">{{ data.description }}</span>
      </div>
    </div>
  </div>
</template>
  
<script>
import axios from "axios";
export default {
  data() {
    return {
      productId: null,
      data: null,
    };
  },
  mounted() {
    // Mengambil ID produk dari objek route
    this.productId = this.$route.params.id;
    axios
      .get(`http://localhost:5500/product/${this.productId}`)
      .then((response) => {
        this.data = response.data.data;
      })
      .catch((err) => {
        console.log(err);
      });
  },
};
</script>

<style scoped>
.scrolling-wrapper {
  overflow-x: scroll;
  overflow-y: hidden;
}
.category {
  border: 1px solid #1794bc;
  background-color: rgba(38, 180, 225, 0.1);
  border-radius: 24px;
  padding: 4px 12px 4px 12px;
  gap: 10px;
  color: rgba(11, 94, 120, 1);
  font-weight: 600;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 0.8em;
  line-height: 18px;
}
.pricey {
  color: rgba(237, 50, 55, 1);
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-weight: 600;
  font-size: 1.3em;
}
</style>
  