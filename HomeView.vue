<template>
  <div class="about-view">
    <h2>About Me</h2>
    <p class="introduction">{{ introduction }}</p>
    <p class="age">Age: {{ age }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      firstName: 'John',
      lastName: 'Doe',
      birthdate: '1990-01-01',
    };
  },
  computed: {
    introduction() {
      return `Hi, I'm ${this.firstName} ${this.lastName}.`;
    },
    age() {
      const birthYear = new Date(this.birthdate).getFullYear();
      const currentYear = new Date().getFullYear();
      return currentYear - birthYear;
    },
  },
};
</script>

<style scoped>
/* Specific styles for the AboutView */
.about-view {
  text-align: center;
  padding: 40px;
}

.about-view h2 {
  font-size: 24px;
  color: #333;
}

.introduction {
  font-size: 18px;
  color: #666;
  margin-top: 20px;
}

.age {
  font-size: 16px;
  color: #999;
}
</style>

.about-view h2 {
  font-size: 24px;
  color: #333;
}

.about-view p {
  font-size: 16px;
  color: #666;
  margin-top: 10px;
}
</style>
