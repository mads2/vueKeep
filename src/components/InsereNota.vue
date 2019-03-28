<template>
  <div class="insereNota">
    <input type="text" rows="2" cols="50"  v-model="mensagemNova" placeholder="Insira nota aqui">
    <button type="button" v-on:click="addevent">OK</button>
  </div>
</template>

<script>
export default {
  name: "criadorDeNota",
  props: ["novaNota"],
  data() {
    return {
      mensagemNova: "",
    };
  },
  methods: {
      addevent(){
          this.$emit('addevent', this.mensagemNova);
            console.log("Aqui ainda vai");
      }
  },
};
</script>

<style scoped>
.insereNota {
  margin-top: 10px;
}
</style>
