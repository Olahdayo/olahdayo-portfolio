<template>
  <section id="contact" class="container my-5">
    <h3 class="section-title">Contact</h3>
    <p class="contact-info">Feel free to reach out to me through any of the platforms below:</p>
    <div class="social-icons">
      <a href="https://facebook.com/booloyede" class="social-icon" target="_blank" rel="noopener noreferrer">
        <i class="fab fa-facebook-f"></i>
      </a>
      <a href="https://twitter.com/olahdayo" class="social-icon" target="_blank" rel="noopener noreferrer">
        <i class="fab fa-twitter"></i>
      </a>
      <a href="https://www.linkedin.com/in/oloyede-blessing-oladayo-b2b541289/" class="social-icon" target="_blank" rel="noopener noreferrer">
        <i class="fab fa-linkedin-in"></i>
      </a>
      <a href="https://github.com/olahdayo" class="social-icon" target="_blank" rel="noopener noreferrer">
        <i class="fab fa-github"></i>
      </a>
      <a href="mailto:blessinoloyede@gmail.com" class="social-icon" target="_blank" rel="noopener noreferrer">
        <i class="fas fa-envelope"></i>
      </a>
      <a href="tel:+2348137386317" class="social-icon" target="_blank" rel="noopener noreferrer">
        <i class="fas fa-phone-alt"></i>
      </a>
    </div>
  </section>
</template>

<script>
export default {

};
</script>

<style scoped>
.section-title {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 1rem;
}

.contact-info {
  text-align: center;
  font-size: 1.2rem;
  margin-bottom: 2rem;
}

.social-icons {
  display: flex;
  justify-content: center;
  gap: 1.5rem;
  flex-wrap: wrap;
}

.social-icon {
  font-size: 2.5rem;
  color: #007bff; 
  transition: transform 0.3s, color 0.3s;
}

.social-icon:hover {
  transform: scale(1.2);
  color: #0056b3; 
}

.social-icon i {
  transition: transform 0.3s;
}
</style>
