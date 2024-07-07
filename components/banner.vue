<template>
  <div class="banner-main">
    <div class="content-area">
      <h2 class="banner-h2">Elevating Your</h2>
      <h1 class="banner-h1">AI  <span>Development</span> Skills </h1>
      <h3 class="banner-h3">A Comprehensive Guide</h3> 
      <p>Artificial Intelligence (AI) is transforming industries with its ability to automate processes and deliver advanced analytics.</p>
      <button class="explore-button">Explore Now!</button>
      <div class="stats">
        <div><span class="data">100+</span><br />Project Complete</div>
        <div><span class="data">50+</span><br />Client Reviews</div>
        <div><span class="data">90+</span><br />5 Star Rating</div>
      </div>
    </div>
    <div class="banner-image-main">
      <NuxtImg src="/images/ai-main1.png" alt="banner" class="banner-img" />
    </div>
  </div>
</template>

<style scoped>
.banner-main {
  position: relative;
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 100%;
      padding: 0 15px;
}
.data {
  font-size: 54px;
  font-weight: 700;
  font-family: "Gilroy-Regular", sans-serif;
}
.content-area {
  max-width: 50%;
  text-align: left;
  color: #fff;
  padding-right: 2rem; /* Add space between image and content */
}

.banner-h2 {
  font-size: 45px;
  font-weight: 600;
  font-family: "Poppins", sans-serif;
  margin-bottom: 10px;
}
.banner-h1 {
  font-size: 53px;
  font-weight: 700;
  font-family: "Poppins", sans-serif;
  margin-bottom: 10px;
  margin-top: 0;
}
.banner-h3 {
  font-size: 53px;
  font-weight: 700;
  font-family: "Poppins", sans-serif;
  margin-bottom: 10px;
  margin-top: 0;
}
.banner-h1 span {
  background: #648DFD;
  background: linear-gradient(to right, #648DFD 52%, #8134FE 46%, #AE56FF 56%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}
.content-area p {
  font-size: 18px;
  font-family: "Gilroy-Regular", sans-serif;
  font-weight: 400;
}

.explore-button {
  background: linear-gradient(135deg, #6c63ff, #a55eea);
  color: #fff;
  border: none;
  padding: 16px 35px;
  font-size: 20px;
  font-weight: 500;
  font-family: "Gilroy-Regular", sans-serif;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s ease;
  max-width: 190px;
  border-radius: 50px;
}

.stats {
  display: flex;
  justify-content: space-between;
  margin-top: 2rem;
}

.stats div {
  text-align: center;
  font-size: 19px;
  font-weight: 500;
  font-family: "Gilroy-Regular", sans-serif;
}

.banner-image-main {
  max-width: 45%;
  position: absolute;
  right: 0;
  top: 0;
  display: flex;
  align-items: center;
}

.banner-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  max-width: 100%;
}

@media (max-width: 767px) {
  .banner-main {
    flex-direction: column;
    text-align: center;
  }

  .content-area {
    max-width: 100%;
  }

  .banner-image-main {
    max-width: 100%;
    position: relative;
  }

  .banner-img {
    width: 80%;
    margin-top: 2rem;
  }

  .stats {
    gap: 1rem;
  }
       .banner-h2 {
  font-size: 24px;
}
.banner-h1 {
  font-size: 28px;
}
.banner-h3 {
  font-size: 28px;
}
.data {
    font-size: 40px;
}
.content-area p{
    font-size: 14px;
            line-height: 1.6;
}
.stats div {
    font-size: 14px;
}
}

@media only screen and (max-width: 1199px) and (min-width: 992px){
  .banner-h2 {
  font-size: 40px;
}
.banner-h1 {
  font-size: 45px;
}
.banner-h3 {
  font-size: 40px;
}
.data {
    font-size: 45px;
}
}
@media only screen and (max-width: 991px) and (min-width: 768px){
    .banner-h2 {
  font-size: 30px;
}
.banner-h1 {
  font-size: 30px;
}
.banner-h3 {
  font-size: 30px;
}
.data {
    font-size: 25px;
}
.stats div{
    font-size: 12px;
}
}

</style>
