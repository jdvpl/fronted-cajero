<template>
        <b-jumbotron
          header="Cajero ATM"
          lead="Facilitamos el crecimiento de tu negocio"
        >
          <p>
            Cajero con los comerciantes, emprendedores y rebuscadores
            Colombianos
          </p>
          <b-button v-b-toggle.sidebar-right type="dark" variant="dark"
            >Mas Informacion</b-button
          >

          <div>
            <b-sidebar
              id="sidebar-right"
              title="Cajero Jdvpl"
              bg-variant="dark"
              text-variant="light"
              right
              shadow
            >
              <div class="px-3 py-2">
                <strong> Facilitamos el crecimiento de tu negocio </strong>
                <p>
                  Cajero con los comerciantes, emprendedores y rebuscadores
                  Colombianos
                </p>
                <b-img
                  src="https://www.elinformador.com.co/images/stories/redes_sociales/2019/12-diciembre/13judinal1.jpg"
                  fluid
                  thumbnail
                ></b-img>
              </div>
            </b-sidebar>
          </div>
        </b-jumbotron>
</template>

<script>
export default {
  name: "Jumbotrom"
}
</script>
