<template>
  <div>
    <div class="container">
      <br />
      <div class="header">
        <img src="../src/assets/unam.png" alt="UNAM" class="unam" />
        <div class="container ">
          <h4>UNIVERSIDAD NACIONAL AUTONOMA DE MEXICO</h4>
          <h4>FACULTAD DE ESTUDIOS SUPERIORES - ACATLAN</h4>
          <h4>CIDWA</h4>
        </div>
      </div>
      <hr>
      <br />
      <div class="text-center">
        <h2><b>Actividad 1:</b> Componente de una Tabla</h2>
      </div>
      <br />
      <h3><b>Ejemplo 1:</b> <i>Arreglo de Objetos [ ]</i></h3>
      <table-component :headers="tableData" :data="tableData" />
      <br />
      <h3><b>Ejemplo 2:</b> <i>API de Crypto-Monedas</i></h3>
      <coins-component />
      <br />
    </div>
    <pie-de-pagina/>
  </div>
</template>

<script>
import CoinsComponent from "./components/CoinsComponent.vue";
import PieDePagina from "./components/PieDePagina.vue";
import TableComponent from "./components/TableComponent.vue";

export default {
  components: {
    TableComponent,
    CoinsComponent,
    PieDePagina,
  },
  data() {
    return {
      tableData: [
        {
          nombre: "Sofia",
          edad: 27,
          correo: "sofia@example.com",
          direccion: "Av Insurgentes 2000, CDMX",
        },
        {
          nombre: "Juan",
          edad: 30,
          correo: "juan@example.com",
          direccion: "San Diego, California",
        },
        {
          nombre: "Pedro",
          edad: 25,
          correo: "pedro@example.com",
          direccion: "Bogota, Colombia",
        },
        {
          nombre: "Laura",
          edad: 22,
          correo: "laura@example.com",
          direccion: "Buenos Aires, Argentina",
        },
      ],
    };
  },
};
</script>

<style scoped>
.unam {
  width: 20vmin;
  height: 20vmin;
}
.header {
  display: inline-flex;
}
.header > div > h4 {
  font-size: 4vmin;
}
</style>
