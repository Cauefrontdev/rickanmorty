<script setup>
import {ref} from 'vue'
</script>

<template>
    <nav class="navbar navbar-expand-lg">
        <div class="container-sm">
          <a class="navbar-brand" href="#"><img src="/src/assets/img/Rick_and_Morty.png" alt=""></a>
          <div class="options">
            <router-link class="button" arial-current="page" to="/">Home</router-link>
            <router-link class="button" arial-current="page" to="/about">Sobre</router-link>
          </div>
        </div>
      </nav>
      <div class="mais"><router-view></router-view></div>
</template>

<style>

.options {
  justify-content: center;
  align-items: center;
  display: flex;
  gap: 20px;
}
     body {
      background-color: black;
    }
    nav img {
      max-width: 250px;
      filter: grayscale();
      filter: brightness(100%);
    }

    nav {
      background-color: black;
    }

    li a {
      color: whitesmoke !important;
    }

    .content {
      display: flex;
      justify-content: center;
      align-items: center;
      height: 80vh;
    }

    .text-box {
      position: relative;
      z-index: 999;
      display: flex;
      flex-direction: column;
      gap: 20px;
    }

    .text-box h1 {
      color: whitesmoke;
      font-size: 4.3rem;
      max-width: 500px;
    }

    .blue {
      color: #00aec6;
    }

    .container {
      overflow: hidden;
      height: 100%;
      display: flex;
      position: relative;
      justify-content: space-between;
      align-items: center;
    }

    .container img {
      position: absolute;
      border-radius: 50%;
      right: -17%;
      max-width: 1200px;
      z-index: 0;
    }

    .green {
      color: #51e681;
      font-size: 25px;
    }

    .info {
      left: 0;
      color: whitesmoke;
      font-size: 20px;
      font-weight: 100;
    }

    .button {
      background-color: black;
      border-radius: 20px;
      border: 1px solid white;
      width: 100px;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 8px;
      transition: 400ms;
    }

    .button:hover {
      background-color: rgb(255, 255, 255);
      color: black !important;
      box-shadow: 0 0 15px #51e68063;
    }

     a {
      text-decoration: none;
      color: whitesmoke !important;
    }
</style>    