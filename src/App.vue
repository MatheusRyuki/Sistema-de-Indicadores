<template>
  <div class="container">
    <div class="login" v-if="isLogged == false">
      <app-login> </app-login>
    </div>
    <div class="dashboard" v-else>
      <app-dashboard></app-dashboard>
    </div>
  </div>
</template>

<script>
  import Login from './components/Login.vue'
  import Dashboard from './components/Dashboard.vue'

export default {
    data () {
      return {
        isLogged: false,
        usuario: ''
      }
    },
    methods: {

    },
    components: {
      appLogin: Login,
      appDashboard: Dashboard
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

  .dashboard {
    background-color: #cecece;
    position: relative;
    margin: 15% auto;
    padding: 2.5%;
  }
</style>



