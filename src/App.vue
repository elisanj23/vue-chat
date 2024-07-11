<template>
  <div id="app">
    <h1 style="font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif ;">Simple Chat App</h1>
    <ChatWindow :messages="messages" />
    <ChatInput @send-message="addMessage" />
  </div>
</template>

<script>
import ChatWindow from './components/ChatWindow.vue';
import ChatInput from './components/ChatInput.vue';

export default {
  name: 'App',
  components: { ChatWindow, ChatInput },
  data() {
    return {
      messages: []
    };
  },
  methods: {
    addMessage(message) {
      this.messages.push(message);
    }
  }
};
</script>

<style>
#app {
  display: flex;
  flex-direction: column;
  max-width: 600px;
  margin: 0 auto;
}
</style>
