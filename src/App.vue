<template>
  <div id="app">
    <Header />
    <div class="layout">
      <Menu />
      <main class="main-content">
        <router-view />
      </main>
    </div>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Menu from "./components/Menu.vue";
import Footer from "./components/Footer.vue";

export default {
  components: {
    Header,
    Menu,
    Footer,
  },
};
</script>

<style>
/* Full page layout */
#app {
  display: flex;
  flex-direction: column;
  height: 100vh;
  font-family: Arial, sans-serif;
  margin: 0;
}

/* Header */
header {
  background: #f5f5f5;
  padding: 10px 20px;
  font-size: 18px;
  font-weight: bold;
  display: flex;
  align-items: center;
  justify-content: flex-start;
  gap: 20px;
  border-bottom: 1px solid #ddd;
}

/* Active page link */
header a {
  text-decoration: none;
  color: black;
}

header a.active {
  color: red;
  font-weight: bold;
}

/* Layout below header */
.layout {
  display: flex;
  flex: 1;
}

/* Menu (Sidebar) */
aside {
  width: 200px;
  background: #efefef;
  padding: 10px;
  border-right: 1px solid #ddd;
}

aside ul {
  list-style: none;
  padding: 0;
}

aside li {
  margin: 10px 0;
  padding: 8px;
  background: #fff;
  text-align: center;
  border: 1px solid #ddd;
  border-radius: 4px;
}

/* Main content area */
.main-content {
  flex: 1;
  padding: 20px;
  text-align: center;
}

/* Footer */
footer {
  background: #f5f5f5;
  padding: 10px 20px;
  text-align: center;
  border-top: 1px solid #ddd;
}
</style>
