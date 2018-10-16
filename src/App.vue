<template>
  <div class="container">
    <div class="login">
      <div>
         <app-login v-if="isLogged == false"> </app-login>
      </div>
    </div>
  </div>
</template>

<script>
  import Login from './components/Login.vue'
export default {
    data () {
      return {
        isLogged: false
      }
    },
    methods: {
    
    },
    components: {
      appLogin: Login
    }
}
</script>


<style>
  body {
    background-color: #E8E9F3;
  }
  .login {
    background-color: #cecece;
    position: relative;
    margin: 15% auto;
    padding: 2.5%;
  }
</style>



