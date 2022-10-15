<template>
  <form @submit.prevent="submitData">
    <div>
      <label>Enter your username: </label>
      <input v-model="userName" type="text"/>
    </div>

    <div>
      <label>Enter your age: </label>
      <input v-model="userAge" type="number"/>
    </div>

    <button>Submit</button>
  </form>

</template>

<script>
export default {
  name: "UserData",
  emits: ['submit-event'],
  data() {
    return {
      userName: '',
      userAge: null
    }
  },
  methods: {
    submitData() {
      this.$emit('submit-event', this.userName, this.userAge)
      this.userName = '';
      this.userAge = null;
    }
  }
}
</script>

<style scoped>

</style>