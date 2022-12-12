<template>
  <div id="app" class="container">
    <formulario-nuevo :listaTabla="listaTabla" @insertarLista="insertarLista" />
    <tabla-lista :listaTabla="listaTabla" />
  </div>
</template>

<script>
import FormularioNuevo from "./components/FormularioNuevo.vue";
import TablaLista from "./components/TablaLista.vue";

export default {
  name: "App",
  components: {
    FormularioNuevo,
    TablaLista,
  },
  data() {
    return {
      listaTabla: [],
    };
  },
  methods: {
    insertarLista(objeto) {
      this.listaTabla.push(objeto);
    },
  },
};
</script>

<style>
body {
  background-color: #eee;
}

#app {
  background-color: white;
  box-shadow: 0px 0px 10px 3px rgba(0.5, 0.5, 0.5, 0.2);
  margin-top: 60px;
  margin-bottom: 60px;
  padding: 60px 30px;
  text-align: left;
}
</style>
