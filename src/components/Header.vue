<template>
  <header class="hero">
    <div class="text-center">
      <h2 class="welcome-message" ref="welcomeMessage"></h2>
      <h1 class="header-title" ref="headerTitle"></h1>
      <h2 class="header-subtitle" ref="headerSubtitle"></h2><hr>
      <p class="header-subtitle mt-0" ref="headerAbout"></p>
      <nav class="nav-buttons">
        <a href="#skills" class="btn btn-primary">Skills</a>
        <a href="#projects" class="btn btn-secondary">Projects</a>
        <a href="#contact" class="btn btn-info">Contact</a>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  mounted() {
    this.typeWriterEffect("Hi🙋‍♂️, I'm", 0, this.$refs.welcomeMessage, () => {
      this.typeWriterEffect("Blessing Oloyede...", 0, this.$refs.headerTitle, () => {
        this.$refs.headerTitle.style.opacity = 1;
        this.typeWriterEffect(
          "Full-Stack Web Developer.",
          0,
          this.$refs.headerSubtitle,
          () => {
            this.$refs.headerSubtitle.style.opacity = 1;
            this.typeWriterEffect(
              "I visualize and bring ideas into accessible websites...",
              0,
              this.$refs.headerAbout,
              () => {
                this.$refs.headerAbout.style.opacity = 1;
              }
            );
          }
        );
      });
    });
  },
  methods: {
    typeWriterEffect(message, index, element, callback) {
      element.style.opacity = 1;
      if (index < message.length) {
        element.innerHTML += message.charAt(index);
        index++;
        setTimeout(
          () => this.typeWriterEffect(message, index, element, callback),
          300
        );
      } else if (callback) {
        callback();
      }
    },
  },
};
</script>

<style scoped>
.hero {
  background: url("/images/geometric-gradient-futuristic-background_23-2149116406.avif")
    no-repeat center center;
  background-size: cover;
  height: 100vh;
  color: white;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  animation: fadeIn 1s ease-in;
  position: relative;
  overflow: hidden;
  animation: backgroundAnimation 30s linear infinite;
}

@keyframes backgroundAnimation {
  0% {
    background-position: center;
  }
  50% {
    background-position: right;
  }
  100% {
    background-position: center;
  }
}

.welcome-message {
  font-size: 2rem;
  margin-bottom: 0.5rem;
  opacity: 0;
  animation: fadeIn 0.8s forwards;
  animation-delay: 0.2s;
}

.header-title {
  font-size: 3rem;
  font-weight: bold;
  margin-bottom: 0.5rem;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7);
  opacity: 0;
}

.header-subtitle {
  font-size: 1.5rem;
  margin-bottom: 2rem;
  text-shadow: 1px 1px 3px rgba(0, 0, 0, 0.5);
  opacity: 0;
}

.nav-buttons {
  display: flex;
  justify-content: center;
  gap: 1rem;
}

.nav-buttons a {
  padding: 10px 20px;
  border-radius: 5px;
  transition: transform 0.3s, background-color 0.3s;
  text-decoration: none;
  font-weight: bold;
}

.nav-buttons a:hover {
  transform: translateY(-5px);
  background-color: rgba(255, 255, 255, 0.2);
}

@keyframes fadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
</style>
