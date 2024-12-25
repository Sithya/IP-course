<template>
  <header>
    <div class="title">Header</div>
    <nav>
      <router-link to="/page1" :class="{ active: isActive('/page1') }"
        >Page 1</router-link
      >
      <router-link to="/page2" :class="{ active: isActive('/page2') }"
        >Page 2</router-link
      >
      <router-link to="/page3" :class="{ active: isActive('/page3') }"
        >Page 3</router-link
      >
    </nav>
  </header>
</template>

<script>
import { useRoute } from "vue-router";

export default {
  setup() {
    const route = useRoute();
    const isActive = (path) => route.path === path;

    return { isActive };
  },
};
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  background: #f5f5f5;
  padding: 10px 20px;
  border-bottom: 2px solid #ddd; /* Add separator line */
}

.title {
  font-size: 18px;
  font-weight: bold;
}

nav {
  display: flex;
  gap: 30px; /* Space between navigation links */
  padding: 10px 0;
}

nav a {
  text-decoration: none;
  color: black;
  font-size: 16px;
  padding: 5px 10px;
  border: 1px solid transparent; /* Default transparent border */
  border-radius: 5px;
  transition: all 0.3s ease;
}

nav a:hover {
  border-color: #ddd;
  background: #f9f9f9;
}

nav a.active {
  color: red;
  border-color: red;
  font-weight: bold;
}
</style>
