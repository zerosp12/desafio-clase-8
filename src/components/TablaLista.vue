<template>
  <div class="table-container">
    <h3>Lista Tabla</h3>
    <div class="table-responsive">
      <table class="table text-center">
        <thead>
          <tr>
            <th scope="col">Nombre</th>
            <th scope="col">Checked</th>
            <th scope="col">País</th>
            <th scope="col">Edad</th>
            <th scope="col">Comentarios</th>
          </tr>
        </thead>
        <tbody>
          <tr v-for="(lista, index) in listaTabla" :key="index">
            <td scope="row">{{ lista.nombre }}</td>
            <td>{{ obtenerChecked(lista.checked) }}</td>
            <td>{{ lista.pais }}</td>
            <td>{{ lista.edad }}</td>
            <td>{{ lista.comentarios }}</td>
          </tr>
        </tbody>
      </table>
    </div>
  </div>
</template>

<script>
export default {
  name: "TablaLista",
  props: {
    listaTabla: Array,
  },
  data() {
    return {};
  },
  methods: {
    obtenerChecked(check) {
      return check ? "Si" : "No";
    },
  },
};
</script>

<style scoped>
.table-container {
  margin-top: 60px;
}
</style>