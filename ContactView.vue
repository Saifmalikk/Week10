<template>
  <div class="contact-view">
    <h2>Contact Me</h2>
    <form @submit.prevent="submitForm" class="contact-form">
      <div class="form-group">
        <label for="name">Name:</label>
        <input type="text" id="name" v-model="formData.name" required />
      </div>
      <div class="form-group">
        <label for="email">Email:</label>
        <input type="email" id="email" v-model="formData.email" required />
      </div>
      <div class="form-group">
        <label for="message">Message:</label>
        <textarea id="message" v-model="formData.message" required></textarea>
      </div>
      <button type="submit">Submit</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      formData: {
        name: '',
        email: '',
        message: '',
      },
    };
  },
  methods: {
    submitForm() {
      // Handle form submission here
      console.log('Form submitted:', this.formData);
      // You can add logic to send the form data to a backend server here
    },
  },
};
</script>

<style scoped>
/* Specific styles for the ContactView */
.contact-view {
  text-align: center;
  padding: 40px;
}

.contact-view h2 {
  font-size: 24px;
  color: #333;
  margin-bottom: 20px;
}

.contact-form {
  max-width: 400px;
  margin: 0 auto;
  text-align: left;
}

.form-group {
  margin-bottom: 20px;
}

label {
  font-size: 18px;
  color: #333;
}

input[type="text"],
input[type="email"],
textarea {
  width: 100%;
  padding: 10px;
  font-size: 16px;
  border: 1px solid #ccc;
  border-radius: 4px;
}

button {
  background-color: #333;
  color: #fff;
  padding: 10px 20px;
  border: none;
  cursor: pointer;
  font-size: 18px;
}

button:hover {
  background-color: #555;
}
</style>
