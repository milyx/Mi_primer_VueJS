<template>
  <div id="app">
    <div class="conteine">
      <div class="row">
        <div class="col-12">
          <h1 class="display-1 my-5">Tabla de usuarios</h1>
        </div>
      </div>
      <div class="row">
        <div class="col-12 px-5">
          <table class="table table-striped">
            <thead>
              <tr>
                <th scope="col">#</th>
                <th scope="col">Nombre</th>
                <th scope="col">Apellido</th>
                <th scope="col">RUN</th>
                <th scope="col">Nacimiento</th>
                <th scope="col">Edad</th>
              </tr>
            </thead>
            <tbody>
              <tr v-for="(usuario, i) in usuarios" :key="i">
                <td>{{ i + 1 }}</td>
                <td>{{ usuario.Nombre }}</td>
                <td>{{ usuario.Apellido }}</td>
                <td>{{ usuario.RUN }}</td>
                <td>{{ usuario.Nacimiento }}</td>
                <td>{{ usuario.Edad }}</td>
              </tr>
            </tbody>
          </table>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      usuarios: [
        {
          Nombre: "Maximiliano",
          Apellido: "Alarcon",
          RUN: "6985697-8",
          Nacimiento: "10-08-1993",
          Edad: 28,
        },
        {
          Nombre: "Daniel",
          Apellido: "Dyvinetz",
          RUN: "27985697-2",
          Nacimiento: "02-05-1985",
          Edad: 36,
        },
        {
          Nombre: "María",
          Apellido: "Rojas",
          RUN: "1485697-7",
          Nacimiento: "25-04-1984",
          Edad: 37,
        },
         {
          Nombre: "Rosa",
          Apellido: "Monasterios",
          RUN: "10852597-2",
          Nacimiento: "05-12-1980",
          Edad: 40,
        },
         {
          Nombre: "Julio",
          Apellido: "Sanchez",
          RUN: "1485697-0",
          Nacimiento: "10-11-1984",
          Edad: 37,
        },
         {
          Nombre: "Francisco",
          Apellido: "Hidalgo",
          RUN: "1285691-3",
          Nacimiento: "02-07-1978",
          Edad: 42,
        },
      ],
    };
  },
  methods: {
    getData() {
      return this.usuarios;
    },
  },
};
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  font-size: 15px;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
