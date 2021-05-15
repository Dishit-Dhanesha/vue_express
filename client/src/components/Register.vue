/* eslint-disable */
<template>
  <div>
    <h1>Register</h1>
    <div>
      <input v-model="email" type="email" id="email" name="email" />
    </div>
    <div>
      <input v-model="password" type="password" id="password" name="password" />
    </div>
    <div>
      <button @click="register" type="submit">Submit</button>
    </div>
  </div>
</template>

<script>
import AuthenticationService from '@/services/AuthenticationService'
export default{
  data () {
    return {
      email: '',
      password: ''
    }
  },
  methods: {
    register () {
      AuthenticationService.register({
        email: this.email,
        password: this.password
      })
    }
  }
}
</script>
