<template>
  <div class="about-main container">
    <div>
      <NuxtImg src="images/about-us.png" alt="about main" class="about-img" />
    </div>
    <div class="about-data">
      <div class="star-data">
        <NuxtImg
          src="images/about-star.png"
          alt="about star"
          class="about-star"
        />
        <h3>About Us</h3>
      </div>

      <h1>AI developers are the future of technology</h1>
      <p>
        Our dedicated team of AI experts, data scientists, and engineers
        collaborates to solve complex problems and deliver cutting-edge
        applications that automate processes and provide profound insights. We
        are committed to continuous learning, ethical AI practices, and
        maintaining the highest standards of quality in our work. Whether you
        seek to leverage AI to enhance your business or wish to join a dynamic
        team passionate about making a difference, we are here to lead the way.
        Join us in shaping a smarter, more connected world.
      </p>
    </div>
  </div>
</template>
<style scoped>
.about-main {
  display: flex;
  justify-content: center;
  align-items: start;
  gap: 3rem;
  margin-top: 140px;
}
.about-data {
  padding: 0 2px;
}
.about-data h3 {
  font-family: "Poppins", sans-serif;
  font-weight: 600;
  font-style: normal;
  font-size: 45px;
  background: #ae56ff;
  background: linear-gradient(to right, #ae56ff 0%, #648dfd 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  margin: 0;
}
.about-data h1 {
  font-family: "Poppins", sans-serif;
  font-weight: 700;
  font-size: 55px;
  color: #222222;
  margin: 15px 0 25px 0;
  text-transform: capitalize;
}
.about-data p {
  font-family: "Gilroy-Regular", sans-serif;
  font-size: 18px;
  color: #222222;
  margin: 0;
  line-height: 1.5;
}
.about-img {
  width: 598px;
  height: 508px;
  object-fit: cover;
}
.star-data {
  display: inline-flex;
  flex-direction: column;
  align-items: flex-start;
  justify-content: space-between;
  height: 100%;
}

.about-star {
  align-self: flex-end;
}
@media only screen and (max-width: 1199px) and (min-width: 992px){
  .about-data h1 {
  font-size: 40px;
}
.about-data p {
  font-size: 15px;
}
}
@media only screen and (max-width: 991px) and (min-width: 768px){
.about-img{
    width: 400px;
    height: auto;
    }
    .about-data h3 {
    font-size: 30px;
    }
    .about-data h1 {
    font-size: 30px;
    }
    .about-main {
    gap: 1rem;
            margin-top: 100px;
    }
    .about-data p {
    font-size: 14px;
}
}
</style>
