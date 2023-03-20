<!-- App.vue (or your main component) -->
<template>
  <div>
    <button @click="toggleModal">Open Modal</button>
    <div v-if="isModalOpen" class="modal">
      <button @click="toggleModal">Close Modal</button>
      <iframe
        title="Walkthrough"
        src="https://example.com/walkthrough-url"
        width="100%"
        height="100%"
      ></iframe>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isModalOpen: false,
    };
  },
  name: "App",
  methods: {
    toggleModal() {
      this.isModalOpen = !this.isModalOpen;
    },
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
