<script setup lang="ts">
import axios from 'axios';
import { ref } from 'vue'

definePageMeta({
  layout: "centered",
});

let nom = ref("")
let email = ref("")

async function obtenirDades() {
  const resposta = await axios.get("/user")
  nom.value = resposta.data.name
  email.value = resposta.data.email
}

obtenirDades()
</script>

<template>
  <p><strong>User Name:</strong> {{ nom }}</p>
  <p><strong>User Email:</strong> {{ email }}</p>
</template>
