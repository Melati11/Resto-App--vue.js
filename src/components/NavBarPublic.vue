<template>
  <nav class="navbar navbar-expand-sm">
    <div class="container-fluid nav-content">
      <div class="logo" v-if="!isMobile">
        <svg
          width="36"
          height="24"
          viewBox="0 0 36 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M31.579 12C31.579 16.1502 28.2629 19.5146 24.1723 19.5146C21.8638 19.5146 19.8021 18.4431 18.4437 16.7637C18.4384 16.8007 18.433 16.8377 18.4273 16.8747C18.2261 18.19 17.7716 19.4523 17.0896 20.5894C16.9516 20.8193 16.8049 21.0433 16.6499 21.2608C18.6943 22.972 21.3149 24 24.1723 24C30.7046 24 36 18.6274 36 12C36 5.37258 30.7046 0 24.1723 0C17.64 0 12.3445 5.37258 12.3445 12C12.3445 15.1997 13.5789 18.1069 15.5908 20.2582C15.6856 20.1191 15.7765 19.9771 15.8634 19.8323C16.4474 18.8586 16.8366 17.7777 17.0089 16.6514C17.155 15.6959 17.1426 14.7236 16.9733 13.7746C16.9372 13.6231 16.9056 13.4699 16.8786 13.315C16.8749 13.2993 16.8712 13.2835 16.8674 13.2678L16.8704 13.2671C16.8015 12.8552 16.7656 12.4318 16.7656 12C16.7656 7.84982 20.0817 4.48544 24.1723 4.48544C28.2629 4.48544 31.579 7.84982 31.579 12Z"
            fill="#96989A"
          />
          <path
            d="M12.6493 14.7367C12.6754 14.9274 12.689 15.1222 12.689 15.3202C12.689 17.6366 10.8381 19.5144 8.55501 19.5144C6.27188 19.5144 4.42104 17.6366 4.42104 15.3202C4.42104 13.0039 6.27188 11.1261 8.55501 11.1261C9.43 11.1261 10.2415 11.4019 10.9097 11.8725C10.9243 10.3059 11.2085 8.74721 11.7559 7.26858C10.7672 6.86359 9.68675 6.64062 8.55501 6.64062C3.83021 6.64062 0 10.5266 0 15.3202C0 20.1139 3.83021 23.9999 8.55501 23.9999C13.2798 23.9999 17.11 20.1139 17.11 15.3202C17.11 12.1975 15.4845 9.45985 13.0452 7.93083C12.325 9.95792 12.1555 12.1466 12.5573 14.2661C12.5893 14.3916 12.6158 14.5195 12.6364 14.6493C12.6428 14.678 12.6492 14.7066 12.6558 14.7352L12.6493 14.7367Z"
            fill="#ED3237"
          />
          <path
            d="M16.8694 13.2675C16.332 11.0197 14.9321 9.11385 13.0453 7.93115C12.5891 9.2151 12.3539 10.5639 12.3448 11.9188C12.3446 11.9459 12.3445 11.973 12.3445 12.0002C12.3445 12.0314 12.3447 12.0626 12.3449 12.0938C12.3505 12.8199 12.421 13.5472 12.5574 14.2664C12.5894 14.392 12.6159 14.5198 12.6364 14.6497C12.6428 14.6783 12.6493 14.7069 12.6559 14.7355L12.6533 14.7361C13.138 16.8448 14.1707 18.7399 15.5908 20.2584C15.6856 20.1193 15.7765 19.9773 15.8633 19.8325C16.4474 18.8588 16.8366 17.7779 17.0089 16.6516C17.0752 16.2178 17.1089 15.7806 17.1101 15.3437C17.1101 15.336 17.1101 15.3283 17.1101 15.3206C17.1101 15.3131 17.1101 15.3056 17.1101 15.2981C17.1087 14.7877 17.0631 14.278 16.9733 13.7748C16.9372 13.6233 16.9056 13.4701 16.8786 13.3152C16.8749 13.2994 16.8712 13.2837 16.8674 13.268L16.8694 13.2675Z"
            fill="#848688"
          />
        </svg>
        <p>Sahaware Digital</p>
      </div>
      <div class="icon">
        <svg
          class="cart"
          width="24"
          height="24"
          viewBox="0 0 24 24"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <g clip-path="url(#clip0_1284_355)">
            <path
              d="M6.5 2H17.5C17.6552 2 17.8084 2.03614 17.9472 2.10557C18.0861 2.175 18.2069 2.2758 18.3 2.4L21 6V21C21 21.2652 20.8946 21.5196 20.7071 21.7071C20.5196 21.8946 20.2652 22 20 22H4C3.73478 22 3.48043 21.8946 3.29289 21.7071C3.10536 21.5196 3 21.2652 3 21V6L5.7 2.4C5.79315 2.2758 5.91393 2.175 6.05279 2.10557C6.19164 2.03614 6.34475 2 6.5 2ZM18.5 6L17 4H7L5.5 6H18.5ZM9 10H7V12C7 13.3261 7.52678 14.5979 8.46447 15.5355C9.40215 16.4732 10.6739 17 12 17C13.3261 17 14.5979 16.4732 15.5355 15.5355C16.4732 14.5979 17 13.3261 17 12V10H15V12C15 12.7956 14.6839 13.5587 14.1213 14.1213C13.5587 14.6839 12.7956 15 12 15C11.2044 15 10.4413 14.6839 9.87868 14.1213C9.31607 13.5587 9 12.7956 9 12V10Z"
              fill="#263137"
            />
          </g>
          <defs>
            <clipPath id="clip0_1284_355">
              <rect width="24" height="24" fill="white" />
            </clipPath>
          </defs>
        </svg>
        <img src="@/assets/avatar.png" alt="avatar" class="avatar" />

        <button class="btn-login">Masuk</button>
        <button class="btn-register">Daftar</button>
      </div>
    </div>
  </nav>
</template>

<script>
export default {
  data() {
    return {
      isMobile: false,
    };
  },
  methods: {
    handleView() {
      this.isMobile = screen.width <= 900;
    },
  },
  beforeMount() {
    this.handleView();
  },
};
</script>

<style>
.nav-content {
  padding: 0 288px;
}

.cart {
  margin-right: 16px;
}

nav {
  background-color: white;
  width: 100vw;
  height: 80px;
  padding: 0 288px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.btn-register {
  background-color: #ed3237;
  border-radius: 6px;
  color: white;
  width: 94px;
  height: 40px;
  border: none;
}

.btn-login {
  border: 1px solid black;
  width: 94px;
  height: 40px;
  border-radius: 4px;
  margin-right: 16px;
}

.avatar {
  display: none;
}

nav .logo {
  display: flex;
  align-items: center;
  gap: 8px;
}

nav .logo p {
  font-weight: 700;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  padding: 0;
  margin: 0;
}

@media screen and (max-width: 576px) {
  .btn-login {
    display: none;
  }
  .btn-register {
    display: none;
  }
  .navbar-brand {
    display: none;
  }
  .avatar {
    display: inline;
    width: 28px;
    height: 28px;
    margin-left: 4px;
  }
  .nav-content {
    justify-content: end;
    padding: 0;
    max-width: 100%;
  }

  nav .icon {
    width: 100vw;
    display: flex;
    justify-content: end;
    padding: 0 16px;
  }
  .cart {
    margin-right: 0;
    width: 28px;
    height: 28px;
    margin-right: 4px;
  }
}
</style>
