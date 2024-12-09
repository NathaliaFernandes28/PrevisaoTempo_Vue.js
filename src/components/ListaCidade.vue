<template>
    <div>
      <h2>Cidade Selecionada: {{ cidadeselecionada}}</h2>
      <div class="lista">
        <Card 
        v-for="cidade in cidades" 
        :key="cidade.id"
        :cidade="cidade"
        v-on:cidadeclicada="mudarcidadeSelecionada"/>
      </div>
    </div>
  </template>
  
  <script>
  import Card from "./Card.vue"
  export default {
    components: {Card},
    methods: {
      mudarcidadeSelecionada(cidade){
        this.cidadeselecionada = cidade.name;
        alert(cidade.name)
      }
    },
      data() {
      return {
        cidadeselecionada: null,
        cidades: [
          {
            id: 8429,
            name: "Rio de Janeiro",
            description: "Ensolarado",
            icon: "01d",
            temp: "35",
          },
          {
            id: 8412,
            name: "Manaus",
            description: "Chuvoso",
            icon: "09d",
            temp: "23",
          },
          {
            id: 8454,
            name: "Brasília",
            description: "Ventania",
            icon: "10d",
            temp: "20",
          },
        ],
      };
    },
  }
  </script>
  
  