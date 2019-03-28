<template>
  <div class="nota">
    <textarea rows="15"  v-model="conteudo" cols="40"></textarea>
    <button class="botao" type="button">Remove</button>
  </div>
</template>

<script>

export default {
  props: ["conteudo"],
  data() {
    return {

    }
  }
};
</script>

<style scoped>
.nota {
  display:  grid;
  max-width: 300px;
  padding: 20px;
  box-shadow: 0px 4px 8px 0px rgba(0, 0, 0, 0.2);
}
.botao {
  max-width: 60%;
  padding: 20px;
  float: right;
  
}

</style>
