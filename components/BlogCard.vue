<template>
  <div class="blog-card">
    <div class="image-wrapper">
      <img :src="`/images/${image}`" :alt="title" />
      <span class="time">{{ time }}</span>
    </div>
    <div class="content">
      <h3 class="card-title">{{ title }}</h3>
      <p class="card-description">{{ description }}</p>
    </div>
  </div>
</template>

<script setup>
defineProps({
  title: String,
  description: String,
  image: String,
  time: String,
});
</script>

<style scoped>
.blog-card {
  background: white;
  border-radius: 15px;
  overflow: hidden;
      box-shadow: 0 4px 8px rgb(114 26 10 / 33%);
  max-width: 550px;
  padding: 15px;
  border: 1px solid #5fc4ecbf;
}

.image-wrapper {
  position: relative;
}

.image-wrapper img {
  height: auto;
  width: 100%;
}

.time {
  position: absolute;
  top: 10px;
  right: 10px;
  background: rgba(0, 0, 0, 0.6);
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 20px;
  font-size: 0.9rem;
}

.content {
  padding: 1rem 1rem 0 1rem;
  text-align: left;
}

.card-title {
  font-size: 22px;
    font-family: "Poppins", sans-serif;
  font-weight: bold;
 margin: 0;
}

.card-description {
  font-size: 18px;
   font-family: 'Gilroy-Regular', sans-serif;
  color: #666;
  line-height: 1.4;
}
@media only screen and (max-width: 1199px) and (min-width: 992px){
.blog-card {
  max-width: 85%;
}
}
@media only screen and (max-width: 991px) and (min-width: 768px){
  .blog-card {
  max-width: 85%;
}
}
@media (max-width: 767px) {
  .card-title {
  font-size: 18px;
}

.card-description {
  font-size: 14px;
}
}
</style>
