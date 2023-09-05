<template>
  <h1>Nome(name): {{ personagem.name }}</h1>
  <h1>Casa(house): {{ personagem.house }}</h1>
  <h1>Patrono(patronus): {{ personagem.patronus }}</h1>
  <img :src="personagem.image" />
</template>
<script setup>
import axios from "axios";
import { ref } from "vue";

const personagem = ref();

// Post - Envia uma requisição
// Get - Pega os dados
console.log("GEt - Faz uma requisição");

axios({
  method: "get",
  url: "https://hp-api.onrender.com/api/characters",
}).then(function (response) {
  let personagens = response.data; //.slice(0, 300);
  personagem.value = personagens[14];
});
</script>
