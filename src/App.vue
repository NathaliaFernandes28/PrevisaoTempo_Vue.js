<template>
  <div>
    <Cabecalho/>
    <ListaCidade/>
  </div>
</template>

<script>
import "./assets/main.css"
import Cabecalho from "./components/Cabecalho.vue";
import ListaCidade from "./components/ListaCidade.vue"



export default {
  components: {
    Cabecalho,
    ListaCidade,
  },
}
</script>



