<template>
  <section class="services-section">
    <div class="container">
      <div class="services-content">
        <h2 class="section-title">
          Our
          <span class="highlight">Services</span>
        </h2>
        <NuxtImg
          src="images/services-star.png"
          alt="services star"
          class="services-star"
        />
      </div>
      <div class="services-grid">
        <div
          class="service-card"
          v-for="(service, index) in services"
          :key="index"
          :class="{ highlighted: service.highlighted }"
        >
          <div :class="['cards-div', { 'white-bg': index === 1 }]">
            <NuxtImg
              :src="service.icon"
              :alt="service.title"
              class="service-icon"
            />
          </div>

          <h3>{{ service.title }}</h3>

          <p>{{ service.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const services = [
  {
    title: "Generative AI",
    description:
      "Generative AI is a fascinating branch of artificial intelligence that focuses on creating new content.",
    icon: "images/services1.png",
    highlighted: false,
  },
  {
    title: "LLM Finetuning",
    description:
      "In the realm of Natural Language Processing (NLP), fine-tuning models like BERT, GPT, and RoBERTa has emerged as a powerful technique to adapt pre-trained language.",
    icon: "images/services2.png",
    highlighted: true,
  },
  {
    title: "Chat Bot",
    description:
      "Empower your business with our advanced chatbot solutions designed to enhance customer experience.",
    icon: "images/services3.png",
    highlighted: false,
  },
  {
    title: "Computer Vision",
    description:
      "Computer vision is a revolutionary field within artificial intelligence that enables machines to interpret visual data.",
    icon: "images/services4.png",
    highlighted: false,
  },
  {
    title: "Speech Recognition",
    description:
      "Speech recognition technology has revolutionized how we interact with devices and applications.",
    icon: "images/services5.png",
    highlighted: false,
  },
  {
    title: "Anomaly Detection",
    description:
      "Anomaly detection is a crucial aspect of data analysis, providing the capability to identify unusual patterns.",
    icon: "images/services6.png",
    highlighted: false,
  },
];
</script>
<style scoped>
.services-section {
  padding: 80px 20px;
  text-align: center;
  background: #f6f6f6;
  margin-top: 150px;
}

.section-title {
  font-family: "Poppins", sans-serif;
  font-weight: 700;
  font-style: bold;
  font-size: 55px;
  display: inline-flex;
  gap: 15px;
  margin-bottom: 0;
  margin-top: 0;
}

.section-title .highlight {
  background: #ae56ff;
  background: linear-gradient(to right, #ae56ff 0%, #648dfd 100%);
  -webkit-text-fill-color: transparent;
  -webkit-background-clip: text;
}

.services-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

.service-card {
  background: #fff;
  border: 1px solid #5fc4ecbf;
  padding: 20px;
  border-radius: 10px;
  transition: all 0.3s ease;
  text-align: center;
}

.service-card.highlighted {
  background: linear-gradient(135deg, #6c63ff, #a55eea);
  color: #fff;
}

.service-card.highlighted .read-more {
  color: #fff;
}

.service-icon {
  width: 63%;
  object-fit: cover;
}

.service-card h3 {
  font-family: "Poppins", sans-serif;
  font-weight: 600;
  font-size: 22px;
  margin-bottom: 10px;
  margin-top: 10px;
}

.service-card p {
  font-size: 16px;
  font-family: "Gilroy-Regular", sans-serif;
  margin-bottom: 0;
  line-height: 1.5;
  padding: 0 11px;
  margin-top: 0;
}

.read-more {
  color: #6c63ff;
  text-decoration: none;
  font-weight: bold;
  transition: color 0.3s ease;
}

.read-more:hover {
  color: #4a42cc;
}

.cards-div {
  background: #ae56ff;
  width: 94px;
  height: 94px;
  border-radius: 50px;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0 auto;
}

.cards-div.white-bg {
  background: #fff;
}
.services-content {
  display: inline-flex;
  flex-direction: column;
  margin-bottom: 40px;
}
@media only screen and (max-width: 1199px) and (min-width: 992px){
  .services-section {
  margin-top: 100px;
}
}
@media only screen and (max-width: 991px) and (min-width: 768px){
  h2.section-title {
    font-size: 35px;
}
.services-section {
    padding: 60px 10px;
    text-align: center;
    background: #f6f6f6;
    margin-top: 100px;
}
.services-grid {
    gap: 10px;
}
.service-card{
    padding: 10px;
}
.cards-div {
    width: 70px;
    height: 70px;
}
.service-card p {
    font-size: 12px;
    padding: 0;

}
}
@media (max-width: 767px) {
.services-grid {
    display: grid;
    grid-template-columns: repeat(1, 1fr);
}
  h2.section-title {
    font-size: 32px;
}
.services-section{
    padding: 60px 0;
}
.services-section {
    margin-top: 100px;
}
}
</style>
