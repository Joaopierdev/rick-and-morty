<script setup>

const character = defineProps(["id","name", "status", "species", "gender", "location", "image", "episodes"])
const id = character.id;
const name = character.name;
const status = character.status;
const specie = character.species;
const gender = character.gender;
const location = character.location.name;
const image = character.image;
const totalEpisodes = character.episodes[0].length;
</script>

<!-- VALUES:
:key="character.id"
:name="character.name"
:status="character.status"
:species="character.species"
:gender="character.gender"
:location="character.location"
:episodes="character.episode" 
-->

<template>
    <div class="col-12 col-md-6" >
        <div class="card card-desktop p-3 mb-4 text-light">
            <div class="cad-img" >
                <img class="cad-img-top image-fluid rounded" :src="image" alt="image character">
            </div>
            <div class="card-body">
                <h3 class="card-tittle">{{ name }}</h3>
                <hr>
                <ul class="list-items">
                    <li class="list-group-item"><i class="bi bi-emoji-grimace-fill"></i> - {{status}}</li>
                    <li class="list-group-item"><i class="bi bi-person-arms-up"></i> - {{specie}}</li>
                    <li class="list-group-item"><i class="bi bi-fingerprint"></i> - {{gender}}</li>
                    <li class="list-group-item"><i class="bi bi-geo-alt-fill"></i> - {{location}}</li>
                    <li class="list-group-item"><i class="bi bi-display-fill"></i> - {{ totalEpisodes }}</li>
                </ul>
            </div>
        </div>
    </div>
</template>

