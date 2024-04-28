<script setup>

const character = defineProps(["id","name", "status", "species", "gender", "location", "image", "episodes"])
const id = character.id;
const name = character.name;
const status = character.status;
const specie = character.species;
const gender = character.gender;
const location = character.location;
const image = character.image;
const totalEpisodes = character.episodes.length;
console.log(totalEpisodes)


</script>

<!-- 
:key="character.id"
:name="character.name"
:status="character.status"
:species="character.species"
:gender="character.gender"
:location="character.location"
:episodes="character.episode" 
-->

<template>
     <!-- <div class="col-md-4" >
        <div class="card mb-3">
            <img :src="imageUrl" height="80" alt="..." class="card-img-top mt-3">
            <p class="text-center" >{{ character.name }}</p>
        </div>
    </div> -->
    <article class="col-md-6" >
            <div class="card p-3 mb-4">
                <div>
                    <img class="cad-img-top" :src="image" width="300px" alt="image character">

                </div>
                <div class="card-body">
                    <h3 class="card-tittle">{{ name }}</h3>
                    <ul></ul>
                </div>
            </div>
            
    </article>
   
</template>

