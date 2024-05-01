<script setup>
const personagem = defineProps(["name", "image", "status", "species", "gender", "location", "episode"])

let statusMap = {
    "Alive": {
        status: "Vivo",
        circle: "green",
        statusColor: "green"
    },
    "Dead": {
        status: "Morto",
        circle: "darkred",
        statusColor: "darkred"
    },
    "unknown": {
        status: "Desconhecido",
        circle: "gray",
        statusColor: "gray"
    },
    "default": {
        statusColor: "black"
    }
}
</script>


<template>
    <div class="col-md-3">
        <div class="card mb-3">
            <div class="card2">
                <img :src="personagem.image">
                <text-box>
                    <h1 class="card-title ">{{ personagem.name }}<br><b id="status">{{ personagem.status }}</b></h1>
                    <p class="card-title"> {{ personagem.species }}, {{ personagem.gender }}</p>
                    <p class="card-title"><i class="bi bi-geo-alt-fill"></i>{{ personagem.location }}</p>
                    <p class="card-title"><b>EPISODES: </b>{{ personagem.episode }}</p>
                </text-box>
            </div>
            
        </div>
    </div>
</template>

<style scoped>
.text-box {
    display: flex;
    flex-direction: column;
    align-items: left;
    text-align: left !;
}
h1 {
    margin-top: 20px;
    font-size: 24px;
    font-weight: 800;
}

b {
    font-size: 14px;
}

i {
    color: #00aec6;
    margin-right: 3px;
}

.card, col-mb-3, mb-3{
    background-color: black !important;
}
.card2 {
  justify-content: left !important;
  align-items: left;
  text-align: left !important;
  color: whitesmoke;
  display: flex;
  flex-direction: column;
  padding: 20px;
  border-radius: 32px;
  background-color: black;
}

.card2 img {
    border-radius: 16px !important;
}
</style>
