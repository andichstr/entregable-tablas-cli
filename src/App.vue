<template>
  <div id="app">
    <h1>Empleados de la empresa</h1>
    <hr><br>
    <h2>Backend</h2>
    <TablaEmpleados :titulos="tabla1.titulos" :registros="tabla1.registros" :clases="tabla1.clases" />
    <br>
    <h2>Frontend</h2>
    <TablaEmpleados :titulos="tabla2.titulos" :registros="tabla2.registros" :clases="tabla2.clases" />
    <br>
    <h2>Recursos Humanos</h2>
    <TablaEmpleados :titulos="tabla3.titulos" :registros="tabla3.registros" :clases="tabla3.clases" />
  </div>
</template>

<script>
import TablaEmpleados from './components/TablaEmpleados.vue'

export default {
  name: 'App',
  components: {
    TablaEmpleados
  },
  data(){
    return{
        tabla1: {
            titulos: ["ID", "Nombre", "Apellido", "Provincia"],
            registros: [
                ["Andres","Schuster","Buenos Aires"],
                ["Lucila", "Fernandez", "Tucuman"],
                ["Julian", "Gomez", "Mendoza"],
                ["Carla", "Perez", "Neuquen"],
            ],
            clases: "fondoAzul letraBlanca",
        },
        tabla2: {
            titulos: ["ID", "Nombre", "Apellido", "Provincia"],
            registros: [
                ["Marcos","Galván","Santa Fe"],
                ["Gustavo", "Lopez", "Tierra del Fuego"],
                ["Barbara", "Gutierrez", "Chaco"],
                ["Sofia", "Vergara", "Misiones"],
            ],
            clases: "fondoGris letraVerde",
        },
        tabla3: {
            titulos: ["ID", "Nombre", "Apellido", "Provincia"],
            registros: [
                ["Martin","Salinas","Tucuman"],
                ["Matias", "Medina", "Buenos Aires"],
                ["Franco", "Sandoval", "Corrientes"],
                ["Julieta", "Venegas", "San Juan"],
            ],
            clases: "fondoMarron letraBlanca",
        }
    }
  }
}

</script>

<style>

  table {
      margin: auto;
      border-color: black;
      width: 600px;
  }

  td, th, thead {
      padding-top: 20px;
      padding-bottom: 20px;
      padding-left: 40px;
      padding-right: 40px;
  }

  table.fondoAzul {
      background-color: blue;
  }

  th.fondoAzul, thead.fondoAzul {
      background-color: black;
  }

  table.fondoGris {
      background-color: rgb(29, 27, 27);
  }

  thead.fondoGris, th.fondoGris {
      background-color: black;
  }

  table.fondoMarron {
      background-color: brown;
  }

  thead.fondoMarron, th.fondoMarron {
      background-color: rgb(63, 21, 21);
  }

  .letraVerde {
      color: green;
      font-weight: bold;
  }

  .letraBlanca {
      color: blanchedalmond;
      font-weight: bold;
  }

  .letraAmarilla {
      color: yellow;
      font-weight: bold;
  }

  h1, h2 {
      text-align: center;
  }

</style>
