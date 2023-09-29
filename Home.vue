<template>
    <div class="home-view">
      <header>
        <h1>Welcome to My Portfolio</h1>
        <p>{{ greetingMessage }}</p>
      </header>
    </div>
  </template>
  
  <script>
  export default {
    data() {
      return {
        greetingMessage: '',
      };
    },
    created() {
      this.setGreetingMessage();
    },
    methods: {
      setGreetingMessage() {
        const now = new Date();
        const hour = now.getHours();
  
        if (hour >= 0 && hour < 12) {
          this.greetingMessage = 'Good morning!';
        } else if (hour >= 12 && hour < 18) {
          this.greetingMessage = 'Good afternoon!';
        } else {
          this.greetingMessage = 'Good evening!';
        }
      },
    },
  };
  </script>
  
  <style scoped>
  /* Specific styles for the HomeView */
  .home-view {
    text-align: center;
    padding: 40px;
    background-color: #f5f5f5;
  }
  
  .home-view header {
    margin-bottom: 20px;
  }
  
  .home-view h1 {
    font-size: 36px;
    color: #333;
    margin-bottom: 10px;
  }
  
  .home-view p {
    font-size: 18px;
    color: #666;
  }
  
  /* Add a stylish background gradient */
  .home-view::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background-image: linear-gradient(135deg, #007BFF, #00BFFF);
    opacity: 0.5;
    z-index: -1;
  }
  
  /* Style the header text */
  header {
    position: relative;
    z-index: 1;
    padding: 20px;
    background-color: rgba(255, 255, 255, 0.8);
    border-radius: 4px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
  }
  
  /* Style the greeting message */
  header p {
    font-weight: bold;
  }
  
  /* Add some padding and border radius to the header */
  header h1 {
    padding: 10px;
    border-radius: 4px;
    background-color: #fff;
    box-shadow: 0px 0px 5px rgba(0, 0, 0, 0.2);
  }
  </style>
  