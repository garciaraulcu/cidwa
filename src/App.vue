<template>
  <div class="container">
    <br>
    <h1>CIDWA</h1>
    <h2>Actividad 1 - Tabla</h2>
    <br>
    <table-component :headers="tableData" :data="tableData"/>
    
  </div>
</template>

<script>
import TableComponent from './components/TableComponent.vue';

export default {
  components: {
    TableComponent,
  },
  data() {
    return {
      tableData: [
        { nombre: 'Sofia', edad: 27, correo: 'frida@example.com', direccion:'Av Insurgentes 2000, CDMX' },
        { nombre: 'Juan', edad: 30, correo: 'juan@example.com', direccion: 'San Diego, California' },
        { nombre: 'Pedro', edad: 25, correo: 'pedro@example.com',direccion: 'Bogota, Colombia' },
        { nombre: 'Laura', edad: 22, correo: 'laura@example.com', direccion: 'Buenos Aires, Argentina'},
      ],
    };
  },
};
</script>
