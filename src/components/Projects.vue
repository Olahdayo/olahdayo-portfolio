<template>
  <section id="projects" class="container my-5">
    <h3 class="section-title">Projects</h3>
    <div class="row">
      <div class="col-md-4 mb-5" v-for="project in projects" :key="project.title">
        <div class="project-card">
          <img :src="project.image" alt="Project Image" class="project-image" />
          <h4 class="project-title">{{ project.title }}</h4>
          <p class="project-description">{{ project.description }}</p>
          <div class="project-buttons">
            <a :href="project.github" class="btn btn-dark">GitHub</a>
            <a :href="project.liveDemo" class="btn btn-success" target="_blank">Live Demo</a>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          title: 'Infinion',
          description: 'A campaign website for users and company, with CRUD functionality...',
          github: 'https://github.com/Olahdayo/infinion_cohort.git',
          liveDemo: 'https://infinion-website.vercel.app/',
          image: '/images/infinion.png',
        },
        {
          title: 'Space-Tourism',
          description: 'A space tourism website with dynamic component rendering built with vue.js...',
          github: 'https://github.com/Olahdayo/Space-Tourism-Website.git',
          liveDemo: 'https://space-tourism-website-flax.vercel.app/',
          image: '/images/spacetourism.png',
        },
        {
          title: 'Product-Listing',
          description: 'An E-commerce website with list of products and cart for item purchase and checkout...',
          github: 'https://github.com/Olahdayo/product-listing.git',
          liveDemo: 'https://product-listing-brown.vercel.app/',
          image: '/images/productlisting.png',
        },
        {
          title: 'FoodApp',
          description: 'Ordering food delicacies of any quantity and varieties from a responsive web app, project done with JS...',
          github: 'https://github.com/Olahdayo/Food-Ordering-App.git',
          liveDemo: 'https://food-ordering-app-one-delta.vercel.app/',
          image: '/images/food.png',
        },
        {
          title: 'Advice QuoteApp',
          description: 'An Advice generator app with random advise generated from an API source...',
          github: 'https://github.com/Olahdayo/Advice-Generator-App.git',
          liveDemo: 'https://advice-app-hazel.vercel.app/',
          image: '/images/advicegen.png',
        },
         {
          title: 'Expense-Tracker',
          description: 'Web Expense Tracker to make list of expenses and keep track of cash flow...',
          github: 'https://github.com/Olahdayo/Expense-Tracker.git',
          liveDemo: 'https://expense-tracker-coral-sigma.vercel.app/',
          image: '/images/expense.png',
        },
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

.project-card {
   background-color: rgba(255, 255, 255, 0.1);
  border-radius: 10px;
  padding: 20px;
  text-align: center;
  transition: transform 0.3s, box-shadow 0.3s;
  margin-bottom: 2rem;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
  display: flex;
  flex-direction: column; 
  height: 100%; 
}

.project-card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.3);
}

.project-image {
  width: 100%;
  height: auto;
  border-radius: 10px;
  margin-bottom: 15px;
  flex-grow: 1;
}

.project-title {
  font-size: 1.5rem;
  margin: 10px 0;
}

.project-description {
  font-size: 1rem;
  margin-bottom: 15px;
  flex-grow: 1;
}

.project-buttons {
  display: flex;
  justify-content: space-between;
}
</style>
