<template>
  <section class="projects">
    <h2>Projects</h2>
    <div class="project" v-for="project in projects" :key="project.id">
      <h3>{{ project.title }}</h3>
      <p>{{ project.description }}</p>
    </div>
  </section>
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
.projects {
  padding: 20px;
}

.project {
  margin-bottom: 20px;
}

.project h3 {
  font-size: 20px;
  color: #333;
}

.project p {
  font-size: 16px;
  color: #666;
}
</style>
