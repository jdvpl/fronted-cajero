<template>
     <b-form class="w-50 m-auto">

          <label class="sr-only" for="inline-form-input-name">Nombre</label>
          <b-input-group prepend="👤" class="mb-2 mr-sm-2 mb-sm-0 sm-12">
            <b-form-input
            type="text"
              id="inline-form-input-username"
              placeholder="Juan Daniel Suarez"
            ></b-form-input>
          </b-input-group><br>
          <label class="sr-only" for="inline-form-input-username"
            >Correo</label
          >
          <b-input-group prepend="✉" class="mb-2 mr-sm-2 mb-sm-0">
            <b-form-input
            type="email"
              id="inline-form-input-username"
              placeholder="jdvpl@gmail.com"
            ></b-form-input>
          </b-input-group><br>

          <b-input-group prepend="🔑" class="mb-2 mr-sm-2 mb-sm-0">
            <b-form-input
            type="password"
              id="inline-form-input-username"
              placeholder="Contraseña"
            ></b-form-input>
          </b-input-group><br>
          <b-button variant="dark" class="btn btn-block">Guardar</b-button>
        </b-form>
</template>

<script>
export default {
  name: "Formulario"
}
</script>
