<template>
  <div>
    <h2>username: {{name}}</h2>
    <h3>age: {{age}}</h3>
  </div>
</template>

<script>
export default {
  name: "ActiveUser",
  props: {
    name: {
      type: String,
      required: true
    },
    age: {
      type: Number,
      required: true
    }
  }
}
</script>

<style scoped>
  div {
    display: inline-block;
    margin: 2rem;
    width: 20vw;
    height: 20vh;
    border-radius: 3%;
    background-color: #4CAF50;
    color: white;
    padding: 1rem;
  }
</style>