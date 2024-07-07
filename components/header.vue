<template>
  <div class="main-header">
    <div class="container">
      <header class="header-area">
        <nav class="nav">
          <input type="checkbox" id="nav-check" v-model="isChecked" />
          <div class="nav-header">
            <div class="nav-title">
              <NuxtLink to="/">
                <NuxtImg src="/images/logo.webp" alt="logo" class="main-logo" />
              </NuxtLink>
            </div>
          </div>
          <ul class="nav-list">
            <li>
              <NuxtLink to="/" @click="closeMenu">Home</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/about-us" @click="closeMenu">About Us</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/services" @click="closeMenu">Services</NuxtLink>
            </li>
            <li>
              <NuxtLink to="/blog" @click="closeMenu">Blog</NuxtLink>
            </li>
          </ul>
          <div class="nav-contact">
            <NuxtLink to="/contact-us" class="contact-button">Contact Us</NuxtLink>
          </div>
          <div class="nav-btn" @click="toggleMenu">
            <label for="nav-check">
              <span></span>
              <span></span>
              <span></span>
            </label>
          </div>
        </nav>
      </header>
      <Banner />
    </div>
    <div class="banner-data">
      <NuxtImg src="/images/bannerdata.png" alt="bannerdata" class="banner-img" />
      <p class="banner-para">
        AI- DEVELOPMENT - AI- DEVELOPMENT - AI- DEVELOPMENT - AI- DEVELOPMENT - AI- DEVELOPMENT - AI- DEVELOPMENT
      </p>
      <p class="banner-para-mobi">
        AI- DEVELOPMENT - AI- DEVELOPMENT - AI- DEVELOPMENT
      </p>
    </div>
  </div>
</template>

<script setup>
const isChecked = ref(false);

const toggleMenu = () => {
  isChecked.value = !isChecked.value;
};

const closeMenu = () => {
  isChecked.value = false;
};
</script>

<style scoped>
.main-header {
  position: relative;
  background: url("/images/banner.jpg") no-repeat center center/cover;
  height: 100%;
  color: #fff;
}

.header-area {
  padding: 24px 15px;
}
.banner-data {
  position: relative;
  display: block;
  bottom: -47px;
}

.banner-img {
  width: 100%;
  height: auto;
  display: block;
}

.banner-para {
  position: absolute;
  top: 50%;
  color: white;
  font-size: 22px;
  text-align: center;
  width: 100%;
  transform-origin: left;
  transform: rotate(358deg);
  margin: 9px 0;
   font-family: "Gilroy-Regular", sans-serif;
}

.nav {
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.nav > .nav-header > .nav-title {
  font-size: 22px;
  color: #fff;
}

.nav > .nav-list {
  gap: 2rem;
}

.nav > .nav-list > li {
  list-style-type: none;
  font-size: 20px;
  font-weight: 600;
  font-family: "Gilroy-Regular", sans-serif;
}

.nav > .nav-list > li a {
  text-decoration: none;
  color: #fff;
  cursor: pointer;
}
.contact-button {
  background: linear-gradient(135deg, #6c63ff, #a55eea);
  color: #fff;
  border: none;
  padding: 16px 45px;
  text-decoration: none;
  font-size: 20px;
  font-weight: 500;
  font-family: "Gilroy-Regular", sans-serif;
  cursor: pointer;
  transition: background-color 0.3s ease;
  max-width: 190px;
  border-radius: 50px;
}

.contact-button:hover {
  background-color: #5753c9;
}

.nav > #nav-check {
  display: none;
}

.nav-btn label {
  cursor: pointer;
  position: relative;
  display: block;
  width: 35px;
  height: 35px;
}
img.main-logo {
  width: 120px;
}
.nav-btn span {
  transition: all 0.2s ease-in-out;
}

#nav-check:checked ~ .nav-btn label span:nth-child(1) {
  transform: rotate(45deg) translate(5px, 5px);
}
#nav-check:checked ~ .nav-btn label span:nth-child(2) {
  opacity: 0;
}
#nav-check:checked ~ .nav-btn label span:nth-child(3) {
  transform: rotate(-45deg) translate(5px, -4px);
}
.banner-para-mobi {
  display: none;
}
@media (max-width: 767px) {
  .banner-data {
    bottom: -20px;
}
  .banner-para-mobi {
  position: absolute;
  top: 50%;
  color: white;
  font-size: 12px;
  text-align: center;
  width: 100%;
  transform-origin: left;
  transform: rotate(358deg);
  margin: 0;
   font-family: "Gilroy-Regular", sans-serif;
   display: block;
}
.banner-para {
display: none;
}
  .banner-para{
    font-size: 12px;
}
  .nav > .nav-list {
    box-shadow: none;
  }
  .nav > .nav-list > li a {
    color: #fff;
  }
  .main-logo {
    max-width: 200px;
  }
  .nav {
    padding: 1rem 0;
  }

  .nav > .nav-btn {
    cursor: pointer;
    border-radius: 4px;
    width: 35px;
    height: 35px;
  }

  .nav > .nav-btn > label {
    display: inline-block;
    width: 50px;
    height: 50px;
    top: 10px;
    position: relative;
    left: 5px;
  }

  .nav > .nav-btn > label > span {
    display: block;
    width: 40px;
    height: 7px;
    border-top: 5px solid #fff;
  }

  .nav > .nav-list {
    position: absolute;
    display: flex;
    flex-direction: column;
    gap: 0;
    width: 100%;
    height: 0;
    transition: all 0.3s ease-in;
    top: 75px;
    left: 0;
    overflow: hidden;
    z-index: 99;
    justify-content: center;
    align-items: center;
    margin: 0 auto;
    background: none;
  }
.nav-contact {
    display: none;
}
  .nav > .nav-list > li {
    width: 100%;
    padding: 15px 0;
    text-align: center;
  }

  .nav > #nav-check:checked ~ .nav-list {
    height: auto;
  }
}

@media (min-width: 768px) and (max-width: 991px) {
  .nav > .nav-list > li a {
    font-size: 14px;
  }
  .nav > .nav-list {
    gap: 0.5rem;
  }
  .main-logo {
    max-width: 240px;
  }
.nav-list {
    padding: 23px 10px !important;
}
.contact-button {
    padding: 16px 30px;
    font-size: 16px;
}
.banner-para{
    font-size: 13px;
}
}

@media (min-width: 768px) {
  .nav-btn {
    display: none;
  }
}
.nav-list {
  list-style: none;
  padding: 23px 34px;
  margin: 0;
  display: flex;
  background: linear-gradient(90deg, #ffffff36, #ffffff36);
  border-radius: 35px;
  box-shadow: inset -5px -8px 250px 0 rgba(255, 255, 255, 0.02);
}

.nav-list li {
  margin: 0 20px;
}

.nav-list li a {
  text-decoration: none;
  color: white;
  font-weight: 500;
  position: relative;
}

.nav-list li a:hover,
.nav-list li a.active {
  color: #7c3aed;
}

.nav-list li a::after {
  content: "";
  display: block;
  width: 0;
  height: 2px;
  background: #7c3aed;
  transition: width 0.3s;
  position: absolute;
  bottom: -5px;
  left: 0;
}

.nav-list li a:hover::after,
.nav-list li a.active::after {
  width: 100%;
}
@media only screen and (max-width: 1199px) and (min-width: 992px){
  .banner-para {
  font-size: 16px;
}
}

</style>
