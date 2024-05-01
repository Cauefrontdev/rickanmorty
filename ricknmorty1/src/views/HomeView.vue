<script setup>
import { onMounted, reactive, ref } from 'vue';
</script>
<template>
  <section class="content">
        <div class="container-sm container">
          <img src="/src/assets/img/rick-and-morty-cartoon-character-rick-sanchez-wallpaper-2048x1152_49.jpg" alt="">
          <div class="text-box">
            <h1><b>Saiba tudo em um só</b> <b class="blue">lugar</b></h1>
            <p class="green">wubba lubba dub dub</p>
            <p class="info">Informações, episódios, personagens,<br> localizações e mais.</p>
            <router-link class="button" arial-current="page" to="/personagens">Ver mais</router-link>
          </div>
        </div>
      </section>

</template>

<style>
    
</style>


