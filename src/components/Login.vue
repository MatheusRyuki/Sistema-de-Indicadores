<template>
<div>
    <h1 class="text-center">Sistema de Indicadores</h1>
    
  <div class="form-group">
    <label for="exampleInputEmail1">Usuário</label>
    <input type="text" class="form-control" id="exampleInputEmail1" v-model="usuarioNow" placeholder="Usuário">
  </div>
  <div class="form-group">
    <label for="exampleInputPassword1">Senha</label>
    <input type="password" class="form-control" id="exampleInputPassword1" placeholder="Senha">
  </div>
  <button  class="btn btn-primary" style="background-color: #272635; margin:1%" v-on:click="Login(true)">Login</button>
  <button class="btn btn-primary" style="background-color: #272635; margin:1%">Cadastrar</button>
</div>
</template>


<script>
export default {
    data() {
        return {
            usuarioNow:''
        }
    },
    methods: {
        Login(value) {
            this.$parent.isLogged = value;
            this.$parent.usuario = this.usuarioNow;
        }
    }
}
</script>


<style>

</style>
