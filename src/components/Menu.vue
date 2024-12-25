<template>
  <aside>
    <ul>
      <li>Section 1</li>
      <li>Section 2</li>
      <li>Section 3</li>
      <li>Section 4</li>
    </ul>
  </aside>
</template>

<script>
export default {};
</script>

<style scoped>
aside {
  width: 200px;
  background: #efefef;
  padding: 10px;
  border-right: 2px solid #ddd; /* Add vertical separator */
}

aside ul {
  list-style: none;
  padding: 0;
  margin: 0;
}

aside li {
  margin: 10px 0;
  padding: 8px;
  background: #fff;
  text-align: center;
  border: 1px solid #ddd;
  border-radius: 4px;
  transition: background 0.3s ease, transform 0.2s ease;
}

aside li:hover {
  background: #e0e0e0;
  transform: scale(1.02);
}
</style>
