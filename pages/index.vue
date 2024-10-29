<script setup lang="ts">
useSeoMeta({
  title: "ViipeR",
  description: "Web Developer, Designer, Freelancer",
});

import { ref } from "vue";

const scrollToSection = () => {
  const section = document.getElementById("getting-started");
  if (section) {
    section.scrollIntoView({ behavior: "smooth" });
  }
};
</script>

<template>
  <NuxtPage />

  <Layout>
    <div class="hero-section">
      <div class="centered-content">
        <h1>Welcome to TaskFinder</h1>
        <p>Your ultimate solution for task management and productivity.</p>

        <a href="#getting-started" @click.prevent="scrollToSection">
          <button class="btn-primary">Get Started</button>
        </a>
      </div>
    </div>

    <div class="container" id="getting-started">
      <h2>Features</h2>
      <br />
      <p>Here are some of the features that TaskFinder offers:</p>
      <br />
      <ul>
        <li>Task Management</li>
        <li>Task Prioritization</li>
        <li>Task Scheduling</li>
        <li>Task Collaboration</li>
      </ul>
    </div>
  </Layout>
</template>

<style scoped>
.hero-section {
  height: 100vh;
  display: flex;
  justify-content: center;
  align-items: center;
  color: white;
  text-align: center;
  padding: 20px;
  width: 100vw;
}

.centered-content {
  max-width: 600px;
  margin: 0 auto;
  padding: 4rem 2rem;
  background: rgba(0, 0, 0, 0.5);
  border-radius: 10px;
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.centered-content h1 {
  font-size: 3em;
  margin-bottom: 20px;
}

.centered-content p {
  font-size: 1.2em;
  margin-bottom: 30px;
}

.btn-primary {
  background-color: #ff7f50;
  color: white;
  padding: 15px 30px;
  border: none;
  border-radius: 25px;
  text-decoration: none;
  font-size: 18px;
  cursor: pointer;
  transition: background-color 0.3s ease, transform 0.3s ease;
}

.btn-primary:hover {
  background-color: #ff4500;
  transform: scale(1.05);
}

.container {
  height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: white;
  padding: 20px;
  width: 100vw;
}
</style>
