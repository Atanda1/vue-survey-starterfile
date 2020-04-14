<template>
  <div id="signup">
    <div id="signin">
     <div class="form">
           <form class="login-form" @submit.prevent="onSubmit">
            <div class="input">
          <input
            type="email"
            placeholder="Email"
            id="email"
            v-model="email">
        </div>
         <div class="input">
          <input
            type="name"
            placeholder="name"
            id="name"
            v-model="name">
        </div>
        <div class="input">
          <input
            type="number"
            id="age"
            placeholder="Age"
            v-model.number="age">       
        </div>
        <div class="input">
          <input
            type="password"
            placeholder="Password"
            id="password"
            v-model="password">
        </div>
        <div class="input">
          <input
            type="password"
            placeholder="Confirm Password"
            id="confirm-password"                 
            v-model="confirmPassword">
        </div>
          <button type="submit">create</button>
          <p class="message">Already registered? <router-link to="/signin">Sign In</router-link></p>
        </form> 
  </div>
  </div>
  </div>
</template>

<script>


export default {
    data () {
      return {
        email: '',
        name: '',
        age: null,
        password: '',
        confirmPassword: ''
      }
    },
     methods : {
       onSubmit () {
        const signupData = {
          name:this.name,
          email: this.email,
          age: this.age,
          password: this.password,
          confirmPassword : this.confimPassword
        }
        console.log(signupData)
      }
     }
}
</script>