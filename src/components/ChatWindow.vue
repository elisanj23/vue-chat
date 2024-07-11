<template>
    <div class="chat-window">
      <Message v-for="(message, index) in messages" :key="index" :message="message" />
    </div>
  </template>
  
  <script>
  import Message from './Message.vue';
  
  export default {
    name: 'ChatWindow',
    components: { Message },
    props: {
      messages: {
        type: Array,
        required: true
      }
    }
  };
  </script>
  
  <style scoped>
  .chat-window {
    height: 300px;
    overflow-y: scroll;
    border: 1px solid #ccc;
    padding: 10px;
  }
  </style>
  