<template>
  <div class="container">    
        <div class="login" v-if="isLogged == false">
          <app-login> </app-login>
        </div>
      <transition name="fade" type="animation">
        <div class="dashboard" v-if="isLogged == true">
          <app-dashboard></app-dashboard>
        </div>
      </transition>
</div>
</template>

<script>
  require('bootstrap')
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

  .fade-enter {
    opacity: 0;
  }

  .fade-enter-active  {
    animation: slide-in 1s ease-out forwards;
    transition: opacity .5s;
  }
  
  .fade-leave-active {
    animation: slide-out 1s ease-out forwards;
    transition: opacity 3s;
    opacity: 0;
  }

  @keyframes slide-in {
    from {
      transform: translateY(0);
    } to {
      transform: translateY(20px);
    }
  }

   @keyframes slide-out {
    from {
      transform: translateY(0);
    } to {
      transform: translateY(20px);
    }
  }
</style>



