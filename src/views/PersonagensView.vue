<template><h1>Personagens</h1></template>
<script setup>
import axios from "axios";

// Post - Envia uma requisição
// Get - Pega os dados
console.log("GEt - Faz uma requisição");

axios({
  method: "get",
  url: "https://hp-api.onrender.com/api/characters",
}).then(function (response) {
  let personagens = response.data.slice(0, 10);
  console.log(personagens[1].name);
});
</script>
