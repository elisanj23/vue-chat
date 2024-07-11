<template>
    <div class="chat-input">
      <input v-model="newMessage" @keyup.enter="sendMessage" placeholder="Type a message..." />
      <button @click="sendMessage">Send</button>
    </div>
  </template>
  
  <script>
  export default {
    name: 'ChatInput',
    data() {
      return {
        newMessage: ''
      };
    },
    methods: {
      sendMessage() {
        if (this.newMessage.trim()) {
          this.$emit('send-message', this.newMessage);
          this.newMessage = '';
        }
      }
    }
  };
  </script>
  
  <style scoped>
  .chat-input {
    display: flex;
    padding: 10px;
  }
  .chat-input input {
    flex: 1;
    padding: 5px;
    border: 1px solid #ccc;
    border-radius: 3px;
  }
  .chat-input button {
    padding: 5px 10px;
    margin-left: 5px;
    border: none;
    background-color: #007bff;
    color: white;
    border-radius: 3px;
    cursor: pointer;
  }
  </style>
  