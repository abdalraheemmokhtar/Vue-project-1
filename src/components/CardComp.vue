<template>
    <div class="card">
      <div>
        <img alt="Vue logo" src="../assets/logo.png">
      </div>
      <div class="card-header">
        <h2>{{ title }}</h2>
      </div>
      <div class="card-content">
        <p>{{ content }}</p>
      </div>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      title: String,
      content: String,
    },
  };
  </script>
  
  <style scoped>
  .card {
    border: 1px solid #ccc;
    border-radius: 4px;
    padding: 16px;
    margin: 16px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
  }
  
  .card-header {
    font-size: 1.2em;
    margin-bottom: 8px;
  }
  
  .card-content {
    font-size: 1em;
  }
  </style>
  