<template>
  <div class="projects-view">
    <h2>Projects</h2>
    <div class="project" v-for="project in projects" :key="project.id">
      <h3>{{ project.title }}</h3>
      <p>{{ project.description }}</p>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      projects: [
        {
          id: 1,
          title: 'Project 1',
          description: 'Description of Project 1.',
        },
        {
          id: 2,
          title: 'Project 2',
          description: 'Description of Project 2.',
        },
        // Add more projects here
      ],
    };
  },
};
</script>

<style scoped>
/* Specific styles for the ProjectsView */
.projects-view {
  text-align: center;
  padding: 40px;
}

.projects-view h2 {
  font-size: 24px;
  color: #333;
  margin-bottom: 20px;
}

.project {
  background-color: #f5f5f5;
  padding: 20px;
  margin-bottom: 20px;
  border-radius: 4px;
  text-align: left;
}

.project h3 {
  font-size: 20px;
  color: #333;
  margin-bottom: 10px;
}

.project p {
  font-size: 16px;
  color: #666;
}
</style>
