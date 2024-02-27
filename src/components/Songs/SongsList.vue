<template>
    <div>
      <!-- Your HTML template code goes here -->
      <h1>Song Title</h1>
      <p>{{ message }}</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'HelloWorld',
    data() {
      return {
        message: 'The songs will go here!'
      };
    },
    // Add other Vue component options here, such as methods, computed properties, etc.
  }
  </script>
  
  <style scoped>
  /* Your component-specific CSS styles go here */
  h1 {
    color: brown;
  }
  p {
    font-size: 18px;
  }
  </style>
  