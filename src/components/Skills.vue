<template>
  <section id="skills" class="container my-5">
    <h3 class="section-title">Skills</h3>
    <div class="skills-list">
      <div class="skill" v-for="skill in skills" :key="skill.name">
        <i :class="skill.icon" class="skill-icon"></i>
        <span class="skill-name">{{ skill.name }}</span>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      skills: [
        { name: 'HTML', icon: 'fab fa-html5' },
        { name: 'CSS', icon: 'fab fa-css3-alt' },
        { name: 'JavaScript', icon: 'fab fa-js' },
        { name: 'Vue.js', icon: 'fab fa-vuejs' },
        { name: 'Git', icon: 'fab fa-git' },
        { name: 'Bootstrap', icon: 'fab fa-bootstrap' },
        { name: 'GitHub', icon: 'fab fa-github' },
        { name: 'PHP', icon: 'fab fa-php' },
        { name: 'MySQL', icon: 'fas fa-database' },
        { name: 'SQL', icon: 'fas fa-database' },
        { name: 'Laravel', icon: 'fab fa-laravel' },
      ],
    };
  },
};
</script>

<style scoped>
.section-title {
  text-align: center;
  font-size: 2.5rem;
  margin-bottom: 1.5rem;
}

.skills-list {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 2rem;
}

.skill {
  background-color: rgba(255, 255, 255, 0.1);
  border-radius: 10px;
  padding: 20px;
  text-align: center;
  transition: transform 0.3s, background-color 0.3s;
  width: 150px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
}

.skill:hover {
  transform: translateY(-5px);
  background-color: rgba(255, 255, 255, 0.2);
}

.skill-icon {
  font-size: 3rem;
  margin-bottom: 10px;
  color: #007bff; 
}

.skill-name {
  font-size: 1.2rem;
  font-weight: bold;
}
</style>
