<template>
  <div>Logging Out...</div>
</template>

<script setup lang="ts">
import axios from 'axios';

await axios.post('/logout')
useRouter().replace("/login")
</script>