<template>
  <div id="app">
    <header-view></header-view>

    <main>
      <!-- Router view to render different views based on the current route -->
      <router-view></router-view>
    </main>

    <footer-view></footer-view>
  </div>
</template>

<script>
import HeaderView from './components/HeaderView.vue';
import FooterView from './components/FooterView.vue';

export default {
  components: {
    HeaderView,
    FooterView,
  },
};
</script>

<style>
/* Reset some default styles */
body {
  margin: 0;
  padding: 0;
  font-family: 'Arial', sans-serif;
  background-color: #f5f5f5;
}

/* Global styles for the entire application */
#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh; /* Ensure the app takes up at least the viewport height */
}

/* Style the header and footer globally */
header-view,
footer-view {
  background-color: #333;
  color: #fff;
  padding: 20px 0;
  text-align: center;
}

/* Style the main content area */
main {
  flex-grow: 1; /* Allow the content to expand and fill available space */
  padding: 20px;
  background-color: #fff;
  box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
  border-radius: 4px;
  margin: 20px 0;
  min-height: 300px; /* Minimum height for content area */
}

/* Style links globally */
a {
  color: #007BFF;
  text-decoration: none;
}

a:hover {
  text-decoration: underline;
}
</style>
