<template>
  <user-data @submit-event="addUser"></user-data>
  <active-user v-for="user in userData" :key="user.id" :name="user.name" :age="user.age"></active-user>
</template>

<script>


export default {
  name: "App",
  data() {
    return {
      userData: []
    }
  },
  methods: {
    addUser(name, age) {
      this.userData.push({
        id: new Date().toISOString(),
        name: name,
        age: age
      })
    }
  }
}
</script>

<style>

form {
  display: grid;
  grid-template-columns: 50% 50%;
  padding: 0 20%;
  column-gap: 5%;
}

input[type=text], [type=number] {
  width: 100%;
  padding: 12px 20px;
  margin: 8px 0;
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}

button {
  width: 30%;
  background-color: #4CAF50;
  color: white;
  padding: 14px 20px;
  margin: 8px 0px;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

button {
  background-color: #45a049;
}

</style>