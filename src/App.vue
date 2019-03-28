<template>
  <div id="app">
    <img src="./assets/notepad.png" height="80" width="80">
    <InsereNota @addevent="addevent"/>
    <div class="notasFlex">
      <Nota v-for="(notinha, index) in notasLista" :key="index" v-bind:conteudo="notinha"></Nota>
    </div>
  </div>
</template>

<script>
import InsereNota from "./components/InsereNota";
import Nota from "./components/Nota";

export default {
  name: "App",
  components: {
    InsereNota,
    Nota
  },
  data() {
    return {
      notasLista: []
    };
  },
  methods: {
     addevent (value) {
      this.notasLista.push(value);
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.notasFlex {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
}
</style>

// notasdb 
// mongodb://notas1:notas1@ds163255.mlab.com:63255/notasdb