<template>
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
</template>

<script>
export default {
  name: "Menu",
   data: function () {
    return {
      is_auth: localStorage.getItem("isAuth") || false,
    };
  },
  methods: {},
    beforeCreate: function () {
    localStorage.setItem("current_username", "JDVPL");
    localStorage.setItem("isAuth", true);
  },
}

</script>
<style>
nav {
  background-color: rgba(0, 0, 0, 0.521) !important;
}
</style>