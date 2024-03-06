<template>
  <div class="home">
    <navbar></navbar>
    <div class="landing">
      <div class="content">
        <p>#New</p>
        <h1>Ngineep Company Profile Website</h1>
        <p>Hospitality Template - One page simple minimalist</p>
        <button class="btn-desktop">Learn More</button>
      </div>
      <div>
        <img src="@/assets/image.png" alt="" />
      </div>
    </div>

    <div class="menu">
      <div class="filter">
        <p>Product Type</p>
        <div class="checkbox">
          <input type="checkbox" name="select" id="select" />
          <label for="select">Company Profile Website</label>
        </div>
      </div>
      <div class="product">
        <router-link
          class="card text-decoration-none"
          v-for="(product, index) in data"
          :key="index"
          :to="{ name: 'ProductDetail', params: { id: product.id } }"
          exact
        >
          <div class="content">
            <img
              :src="`./assets/${product.image_url}`"
              class="product-img img-fluid"
              alt=""
              style="border-radius: 10px"
            />
            <h3>{{ product.name }}</h3>
            <p>Rp. {{ product.price }}</p>
          </div>
        </router-link>
      </div>
    </div>

    <!-- <div class="product">
      <div class="filter">
        <p>Product Type</p>
        <div class="checkbox">
          <input type="checkbox" name="type" id="type" />
          <h5>Compeny Profile Website</h5>
        </div>
      </div>
      <div class="menu 9">
        <router-link
          class="card text-decoration-none"
          v-for="(product, index) in data"
          :key="index"
          :to="{ name: 'ProductDetail', params: { id: product.id } }"
          exact
        >
          <div>
            <img src="@/assets/test.jpg" class="product-img img-fluid" alt="" />
            <h3>{{ product.name }}</h3>
            <p>Rp. {{ product.price }}</p>
          </div>
        </router-link>
      </div>
    </div> -->
  </div>
</template>

<style scoped>
* {
  margin: 0;
  padding: 0;
}
.landing {
  background-color: #f1f1f1;
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0 240px;
}

.landing .content {
  width: 774px;
  height: 243px;
}

.landing .content h1 {
  font-size: 42px;
  font-weight: 700;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  margin-bottom: 24px;
}

.landing .content p:first-child {
  margin-bottom: 16px;
  color: #ed3237;
  font-weight: 400;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 16px;
}

.landing .content p {
  margin-bottom: 32px;
  font-size: 24px;
  font-weight: 700;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}

.landing .content button {
  padding: 12px 48px;
  background-color: #ed3237;
  border-radius: 6px;
  border: none;
  color: white;
  font-size: 16px;
  font-weight: 600;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}
.landing img {
  width: 400px;
  border-radius: 16px;
}

.menu {
  margin-top: 100px;
  display: flex;
  padding: 0 48px;
}

.menu .filter {
  width: 33.5%;
}

.menu .filter .checkbox {
  display: flex;
  align-items: center;
  margin-top: 24px;
  gap: 10px;
}

.menu .filter p {
  font-weight: 600;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 18px;
  color: #00000080;
}

.menu .filter .checkbox label {
  font-weight: 600;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 18px;
}

.menu .product {
  display: flex;
  flex-wrap: wrap;
  gap: 15px;
  width: 1356px;
}

.menu .product img {
  width: 350px;
}

.menu .product h3 {
  margin-top: 20px;
  font-size: 25px;
  font-weight: 400;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}

.menu .product p {
  font-size: 18px;
  font-weight: 400;
  color: #00000099;
  margin-top: 13px;
}

.card .content {
  overflow: hidden;
}

.card {
  overflow: hidden;
  border: none;
}
/* 
.product {
  margin-top: 100px;
  align-items: center;
  display: flex;
  flex-wrap: wrap;
  width: 100vw;
  justify-content: space-between;
  background-color: #ed3237;
}

.filter {
  margin-top: 24px;
}

.product .filter p {
  font-weight: 600;
  font-size: 18px;
  color: #00000080;
}

.product .filter h5 {
  font-weight: 600;
  font-size: 18px;
  margin-bottom: 0;
}

.menu {
  display: flex;
  flex-wrap: wrap;
  margin-left: 222px;
  background-color: aqua;
  width: 80%;
}

.row {
  display: flex;
  gap: 24px;
}

.checkbox {
  display: flex;
  align-items: center;
  gap: 8px;
}

.menu .card {
  overflow: hidden;
  border: none;
  border-radius: 4px;
  width: 330px;
}

.menu .card h3 {
  margin-top: 19px;
  font-size: 25.35px;
  font-weight: 400;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  text-decoration: none;
}

.menu .card p {
  margin-top: 13px;
  color: #00000099;
  font-weight: 400;
  font-size: 18px;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}

.menu img {
  width: 100%;
  object-fit: cover;
  text-decoration: none;
  border-radius: 4px;
}
.btn-mobile {
  display: none;
} */
</style>

<script>
import axios from "axios";
import Navbar from "@/components/NavBarPublic.vue";

export default {
  name: "HomeView",
  components: { Navbar },
  data() {
    return {
      data: null,
    };
  },
  mounted() {
    axios
      .get("http://localhost:5500/product")
      .then((response) => {
        this.data = response.data.data;
      })
      .catch((err) => {
        console.log(err);
      });
  },
};
</script>
