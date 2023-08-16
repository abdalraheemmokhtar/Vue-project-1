<template>
    <form @submit.prevent="submitForm">
      <div class="form-group">
        <label for="name">Name:</label>
        <input v-model="name" type="text" id="name" required>
      </div>
      <div class="form-group">
        <label for="email">Email:</label>
        <input v-model="email" type="email" id="email" required>
      </div>
      <button type="submit">Submit</button>
    </form>
  </template>
  
  <script>
  export default {
    data() {
      return {
        name: '',
        email: ''
      };
    },
    methods: {
      submitForm() {
        this.$emit('form-submitted', { name: this.name, email: this.email });
        this.name = '';
        this.email = '';
      }
    }
  };
  </script>
  
  <style>
  .form-group {
    margin-bottom: 1rem;
  }
  </style>
  