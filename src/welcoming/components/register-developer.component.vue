<script>
export default {
  name: "register-developer.component",

  data() {
    return {
      firstName: '',
      lastName: ''
    }
  },

  methods: {
    onSubmit() {
      console.log('Registering Developer');
      this.$emit('developer-registered', {
        firstName: this.firstName,
        lastName: this.lastName
      });
    }
  }
}
</script>

<template>
  <div>
    <h1>New Developer</h1>
    <div>
      <form @submit.prevent="onSubmit"></form>
      <div>
        <label for="firstName">First Name</label>
        <input type="text" id="firstName" v-model="firstName" required/>
      </div>
      <div>
        <label for="lastName">Last Name</label>
        <input type="text" id="lastName" v-model="lastName" required/>
      </div>
      <div>
        <button type="submit">Register</button>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>