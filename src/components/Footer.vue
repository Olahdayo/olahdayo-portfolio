<template>
  <footer class="footer text-center py-4">
    <div class="profile-pic-container">
      <img
        src="/public/images/WhatsApp Image 2024-11-19 at 12.26.50_3a6a0a79.jpg"
        alt="Profile Picture"
        class="profile-pic"
      />
    </div>
    <p>&copy; {{ currentYear }} Olahdayo. All rights reserved.</p>
  </footer>
</template>

<script>
export default {
  data() {
    return {
      currentYear: new Date().getFullYear(), 
    };
  },
};
</script>

<style scoped>
.footer {
  background-color: #343a40; 
  color: white;
  padding: 20px 0;
  position: relative;
}

.profile-pic-container {
  margin-bottom: 10px;
}

.profile-pic {
  width: 100px; 
  height: 100px; 
  border-radius: 50%; 
  border: 3px solid #007bff; 
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3); 
}

.footer p {
  margin: 0;
  font-size: 1rem;
}
</style>
