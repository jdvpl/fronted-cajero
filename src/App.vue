<template>
  <div id="app">
    <div class="header">
      <div>
        <b-navbar toggleable="sm" type="dark" variant="dark">
          <b-navbar-toggle target="nav-text-collapse"></b-navbar-toggle>
          <b-navbar-brand class="font-weight-bold mr-5"
            >Cajero Api</b-navbar-brand
          >
          <b-collapse id="nav-text-collapse" is-nav>
            <b-navbar-nav class="text-center">
              <b-nav-item v-on:click="init" v-if="is_auth">Inicio</b-nav-item>
              <b-nav-item v-on:click="getBalance" v-if="is_auth">Saldo</b-nav-item>
              <b-nav-item v-if="is_auth">Transaccion</b-nav-item>
              <b-nav-item v-if="is_auth">Cerrar Sesion</b-nav-item>
            </b-navbar-nav>
          </b-collapse>
        </b-navbar>
      </div>
    </div>
    <div class="text-center">
       <jumbotrom></jumbotrom>
    </div>
    <div class="main-component text-center">
      <router-view></router-view>
    </div>

    <div class="footer">
      <div class="d-flex bg-dark text-light align-items-center px-3 py-3">
        <strong class="m-auto">Desarrollado por: Juan Daniel Suarez</strong>
      </div>
    </div>
  </div>
</template>

<script>
import Jumbotrom from './components/Jumbotrom.vue'
export default {
  name: 'App',
  components:{Jumbotrom},
  
  data:function() {
    return {
      is_auth:localStorage.getItem('isAuth') || false
    }
  },
  
  methods: {
    init: function(){
      if(this.$route.name != "user"){
        let username = localStorage.getItem("current_username")
        this.$router.push({name: "user", params:{ username: username }})
      }
    },
    getBalance: function(){
      if(this.$route.name != "user_balance"){
        let username = localStorage.getItem("current_username")
        this.$router.push({name: "user_balance", params:{ username: username }})
      }
    },
  },
  beforeCreate:function() {
    localStorage.setItem('current_username','camilo24')
    localStorage.setItem('isAuth',true)
    this.$router.push({name: "user", params:{ username: 'camilo24' }})  
  }
}
</script>


<style>
body {
  margin: 0 0 0 0;
}

nav {
  background-color: rgba(0, 0, 0, 0.521) !important;
}
.footer {
  bottom: 0;
  position: fixed;
  width: 100%;
  text-align: center !important;
}
</style>
