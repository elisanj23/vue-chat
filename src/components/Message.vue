<template>
    <div class="message">
      <p>{{ message }}</p>
    </div>
  </template>
  
  <script>
  export default {
    name: 'Message',
    props: {
      message: {
        type: String,
        required: true
      }
    }
  };
  </script>
  
  <style scoped>
  .message {
    padding: 5px 10px;
    border-bottom: 1px solid #ccc;
  }
  </style>
  