<template>
  <button class="button1" @click="handleClick">
    {{ label }}
  </button>
</template>

<script>
export default {
  props: {
    label: {
      type: String,
      default: "SOME BUTTON"
    }
  },
  methods: {
    handleClick() {
      // You can add custom click handling logic here
      console.log(`Button "${this.label}" clicked`);
    }
  }
};
</script>

<style scoped>
/* Add your component-specific styles here */
.button1 {
  background-color: #3498db;
  color: #ffffff;
  border: none;
  padding: 10px 20px;
  cursor: pointer;
  border-radius: 5px;
  font-size: 16px;
}

.button1:hover {
  background-color: #2980b9;
}
</style>
