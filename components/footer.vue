<template>
  <footer class="footer">
    <div class="social-icons">
      <a href="https://facebook.com" target="_blank" class="icon">
        <NuxtImg src="/images/facebook.png" alt="facebook" class="facebook"
      /></a>
      <a href="https://instagram.com" target="_blank" class="icon">
        <NuxtImg src="/images/insta.png" alt="insta" class="insta"
      /></a>
      <a href="#" class="icon">
        <NuxtImg src="/images/twitter.png" alt="twitter" class="twitter"
      /></a>
    </div>
    <div class="copyright">© 2024 by AI Developer All rights reserved!</div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped>
.footer {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px 46px;
  background-color: #a259ff;
  color: white;
}

.social-icons {
  display: flex;
  gap: 30px;
}

.icon {
  color: white;
  font-size: 1.5rem;
  text-decoration: none;
}

.icon:hover {
  color: #cccccc;
}

.copyright {
  font-size: 18px;
  font-family: "Poppins", sans-serif;
}
img.insta {
  width: 23px;
}
img.facebook {
    width: 12px;
}
img.twitter {
    width: 20px;
}
</style>
