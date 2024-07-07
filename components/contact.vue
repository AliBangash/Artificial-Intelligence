<template>
  <div class="contact-form container">
    <div class="form-container">
      <div class="image-container">
        <img src="/images/contact-us.png" alt="Contact Us Image" />
      </div>
      <div class="form-content">
        <h2>Contact Us</h2>
        <p>Lorem ipsum dolor sit amet consectetur.</p>
        <form @submit.prevent="handleSubmit">
          <div class="form-group">
            <input
              type="text"
              v-model="form.name"
              placeholder="Name"
              required
            />
          </div>
          <div class="form-group">
            <input
              type="email"
              v-model="form.email"
              placeholder="Email"
              required
            />
          </div>
          <div class="form-group">
            <textarea
              v-model="form.message"
              placeholder="Message"
              required
            ></textarea>
          </div>
          <button type="submit" class="submit-button">Submit</button>
        </form>
      </div>
    </div>
  </div>
</template>

<script setup>
const form = reactive({
  name: "",
  email: "",
  message: "",
});

const handleSubmit = () => {
  console.log("Form submitted", form);
};
</script>

<style scoped>
.form-container {
  display: flex;
  border-radius: 8px;
  overflow: hidden;
  padding: 40px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
  background: #f6f6f6;
  gap: 40px;
  margin-bottom: 140px;
}

.image-container img {
  width: 100%;
  height: auto;
}

.form-content h2 {
  margin-bottom: 10px;
  font-weight: 700;
  font-family: "Poppins", sans-serif;
  font-size: 56px;
}

.form-content p {
  margin-bottom: 20px;
  color: #333333;
  font-weight: 400;
  font-family: "Gilroy-Regular", sans-serif;
  font-size: 18px;
}

.form-group {
  margin-bottom: 15px;
}

input,
textarea {
  width: 100%;
  padding: 10px 30px;
  border: 1px solid #b4a4a4;
  border-radius: 4px;
  width: 508px;
  height: 79px;
  border-radius: 13px;
  outline: none;
}

.submit-button {
  background: linear-gradient(135deg, #6c63ff, #a55eea);
  color: #fff;
  border: none;
  padding: 16px 64px;
  text-decoration: none;
  font-size: 20px;
  font-weight: 500;
  font-family: "Gilroy-Regular", sans-serif;
  cursor: pointer;
  transition: background-color 0.3s ease;
  max-width: 190px;
  border-radius: 50px;
}

.submit-button:hover {
  background-color: #2575fc;
}
@media only screen and (max-width: 1199px) and (min-width: 992px){
  input,
textarea {
  width: 350px;
  height: 45px;
}
.form-content h2 {
  font-size: 45px;
}
.form-container {
    margin-bottom: 100px;
}
}
@media only screen and (max-width: 991px) and (min-width: 768px){
    input,
textarea {
  width: 180px;
  height: 35px;
}
.form-content h2 {
  font-size: 35px;
}
.form-container {
    margin-bottom: 100px;
}
}
</style>
