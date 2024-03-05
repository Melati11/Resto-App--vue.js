<template>
  <div class="home">
    <div class="landing">
      <div class="content">
        <h1 class="mobile-h1">Ngineep Company Profile Website</h1>
        <p class="mobile-p">
          Hospitality Template - One page simple minimalist
        </p>
        <button class="btn-desktop">Learn More</button>
      </div>
      <div>
        <img src="@/assets/image.png" alt="" />
        <button class="btn-mobile">Learn More</button>
      </div>
    </div>

    <div class="container">
      <div class="product">
        <div class="filter col-lg-3">
          <p>Product Type</p>
          <div class="checkbox">
            <input type="checkbox" name="type" id="type" />
            <h5>Compeny Profile Website</h5>
          </div>
        </div>
        <div class="menu col-lg-9">
          <div class="row">
            <router-link
              class="card text-decoration-none col-lg-4 gx-3"
              v-for="(product, index) in data"
              :key="index"
              :to="{ name: 'ProductDetail', params: { id: product.id } }"
              exact
            >
              <div>
                <img
                  src="@/assets/test.jpg"
                  class="product-img img-fluid"
                  alt=""
                />
                <h3>{{ product.name }}</h3>
                <p>Rp. {{ product.price }}</p>
              </div>
            </router-link>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
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
}

.landing .content p {
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

.product {
  margin-top: 100px;
  display: flex;
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
  width: 1, 356px;
  display: flex;
  flex-wrap: wrap;
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
}
@media screen and (max-width: 576px) {
  .landing {
    padding: 0;
    display: block;
    padding: 5%;
    height: 110vh;
  }
  .mobile-h1 {
    width: 40%;
    line-height: 63px;
    margin-bottom: 24px;
  }
  .mobile-p {
    width: 40%;
    margin-bottom: 40px;
  }
  .btn-desktop {
    display: none;
  }
  .btn-mobile {
    display: block;
    margin: auto;
    padding: 12px 48px;
    background-color: #ed3237;
    border-radius: 6px;
    border: none;
    color: white;
    margin-top: 24px;
    font-size: 16px;
    font-weight: 600;
    font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
    width: 328px;
  }
  .landing img {
    display: flex;
    margin: auto;
    width: 328px;
  }
  .landing .content {
    width: 774px;
    height: fit-content;
  }
  .filter {
    display: none;
  }
  .menu .card {
    width: 50%;
    margin: auto;
  }
  .product {
    margin-top: 24px;
  }
  .menu {
    padding: 0 19px;
  }
}
</style>

<script>
import axios from "axios";

export default {
  name: "HomeView",
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
