<template>
  <div class="form">
    <div class="container">
      <h2 class="text-left">Datos personales</h2>
      <div class="row">
        <div class="col-lg-4">
          <div class="form-group">
            <label for="nombre">Nombre</label>
            <input
              type="text"
              class="form-control"
              id="nombre"
              placeholder="Ingrese su nombre"
              name="nombre"
            />
          </div>
        </div>
        <div class="col-lg-4">
          <div class="form-group">
            <label for="cedula">Cédula:</label>
            <input
              type="string"
              class="form-control"
              id="cedula"
              placeholder="cédula"
              name="cedula"
            />
          </div>
        </div>
        <div class="col-lg-4">
          <label for="Facultad">Facultad:</label>
          <select name="facultad" class="custom-select">
            <option selected>Selecione su facultad</option>
            <option value="derecho">Derecho</option>
            <option value="sistema">Sistema</option>
            <option value="medicina">Medicina</option>
          </select>
        </div>
      </div>

      <div>
        <div class="row">
          <div class="col-lg-4">
            <select name="genero" class="custom-select">
              <option selected>Selecione su genero</option>
              <option value="hombre">Hombre</option>
              <option value="mujer">Mujer</option>
            </select>
          </div>
          <button v-on:click="agregar" type="button" class="btn btn-primary">Enviar</button>
          <div class="col-lg-4">
            <table class="table table-dark table-striped">
              <thead>
                <tr>
                  <th>Nombre</th>
                  <th>Cedula</th>
                  <th>Facultad</th>
                  <th>Sexo</th>
                </tr>
              </thead>
              <tbody>
                <tr v-for="(item, index) in info" :key="index">
                  <td>{{ item.nombre }}</td>
                  <td>{{ item.cedula }}</td>
                  <td>{{ item.Facultad }}</td>
                  <td>{{ item.genero }}</td>
                </tr>
              </tbody>
            </table>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "formulario",
   data() {
    return {
      nombre: "",
      cedula: "",
      facultad: "",
      genero: "",
      info: [
        {
          nombre: "",
          cedula: "",
          facultad: "",
          genero: "",
        }
      ]
    };
  },
  methods: {
    agregar() {
      this.info.push({
        nombre: this.nombre,
        cedula: this.cedula,
        carrofacultad: this.facultad,
        genero: this.genero,

      });
      console.log(this.usuario);
    }
  }
};
</script> 
};
</script>
