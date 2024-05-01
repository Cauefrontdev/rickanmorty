<script setup>
import { onMounted, reactive, ref } from 'vue';
import ListPersonagens from '../components/ListPersonagens.vue';
let personagens = reactive(ref());

onMounted(() => {
  fetch("https://rickandmortyapi.com/api/character/?page=1")
  
  .then(response => response.json())
  .then(response => {
    personagens.value = response.results;
    console.log(personagens);
  });
});
</script>
<template>
  <main>
    <div class="container-sm">
      <div class="row mt-4">
        <div class="col-sm-12 col-md-12" >
            <div class="card-body row" >

              <ListPersonagens
              v-for="personagem in personagens"
              :key="personagem.id"
              :name="personagem.name"
              :image="personagem.image"
              :status = "personagem.status"
              :species = "personagem.species"
              :gender = "personagem.gender"
              :location = "personagem.location.name"
              :episode = "personagem.episode.length"
            ></ListPersonagens>
            
          </div>
        </div>
      </div>
    </div>
  </main>
</template>


