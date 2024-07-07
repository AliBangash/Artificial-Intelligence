<template>
  <section class="blog-section">
    <div>
      <div class="header-data container">
        <div class="blog-title">
          <h2 class="title">Blog About</h2>
          <h2 class="title-data">Development</h2>
        </div>
        <div class="blog-content">
          <p class="description">
            Explore the latest insights, trends, and developments in artificial
            intelligence with our informative and engaging blogs. Our team of AI
            experts regularly publishes articles on various topics.
          </p>
          <a href="#" class="explore-button">Explore Now!</a>
        </div>
      </div>
      <div class="blog-cards">
        <BlogCard
          title="Demystifying Deep Learning Networks"
          description="Delve into the world of deep learning as we unravel the complexities of neural networks. In this blog, we break down the fundamentals of deep learning, explore the architecture of neural networks, and discuss real-world applications that showcase their power and versatility."
          image="/blog1.png"
          time="7 Min Added"
        />
        <div class="blog-subdata">
          <BlogCard
            title="The Evolution Of Natural Language Processing"
            description="Join us on a journey through the evolution of natural language processing (NLP) as we trace its development."
            image="blog2.png"
            time="7 Min Added"
          />
          <BlogCard
            title="Unleashing The Power Of Computer Vision"
            description="Unlock the potential of computer vision as we explore its applications and discuss emerging that are shaping its future."
            image="blog3.png"
            time="7 Min Added"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.blog-section {
  margin: 140px 0;
}
.title-data {
  font-family: "Poppins", sans-serif;
  font-weight: 700;
  font-style: normal;
  font-size: 55px;
  background: #ae56ff;
  background: linear-gradient(to right, #ae56ff 0%, #648dfd 100%);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
  margin: 0;
}
.header-data {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 15px;
}

.title {
  font-family: "Poppins", sans-serif;
  font-weight: 700;
  font-style: normal;
  font-size: 55px;
  margin-bottom: 10px;
  margin-top: 0;
  display: flex;
}
.description {
  font-size: 18px;
  color: #666;
  font-family: "Gilroy-Regular", sans-serif;
  line-height: 1.5;
  max-width: 590px;
  text-align: start;
}

.explore-button {
  padding: 18px 0px;
  background: linear-gradient(135deg, #6c63ff, #a55eea);
  color: white;
  border-radius: 30px;
  text-decoration: none;
  font-weight: bold;
  max-width: 190px;
  margin-top: 10px;
  text-align: center;
}

.blog-cards {
  display: flex;
  gap: 1.5rem;
  justify-content: center;
  flex-wrap: wrap;
  padding-top: 55px;
}
.blog-content {
  flex-direction: column;
  display: flex;
}
.blog-subdata {
  gap: 1.5rem !important;
  display: flex;
  flex-direction: column;
}
@media only screen and (max-width: 1199px) and (min-width: 992px) {
  .blog-cards {
    flex-direction: column;
    justify-content: center;
    align-items: center;
  }
  .header-data {
    padding: 0 40px;
  }
  .blog-section {
    margin: 100px 0;
  }
  .blog-subdata {
    justify-content: center;
    align-items: center;
  }
}
@media only screen and (max-width: 991px) and (min-width: 768px) {
  .blog-section {
    margin: 100px 0;
  }
  .title {
    font-size: 35px;
  }
  .title-data {
    font-size: 35px;
  }
  .description {
    font-size: 14px;
  }
  .header-data {
    padding: 0 25px;
    gap: 4rem;
  }
  .blog-subdata {
    justify-content: center;
    align-items: center;
  }
}
@media (max-width: 767px) {
  .header-data.container {
    flex-direction: column;
    align-items: start;
    padding: 0 30px;
  }
  .title {
    font-size: 32px;
  }
  .title-data {
    font-size: 32px;
  }
  .description {
    font-size: 14px;
  }
  .blog-cards {
    padding: 55px 30px 0 30px;
}
.blog-section {
    margin: 100px 0;
}
}
</style>
