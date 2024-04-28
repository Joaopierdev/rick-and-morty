<script setup>
  import { onMounted, reactive, ref } from 'vue';
  import ListRickAndMorty from '../components/ListRickAndMorty.vue';

  let characters = reactive(ref());

  onMounted(()=>{
    fetch("https://rickandmortyapi.com/api/character/?page=1")
    .then(response => response.json())
    .then(response =>{
      characters.value = response.results
      console.log(characters)

    })
  
  })

</script>

<template>
  <main>
    <div class="container">
      <div class="row mt-4">
        <ListRickAndMorty
                v-for="character in characters"
                :key="character.id"
                :name="character.name"
                :status="character.status"
                :species="character.species"
                :gender="character.gender"
                :location="character.location"
                :image="character.image"
                :episodes="[character.episode]"
              />
        <!-- <div class="col-12 col-md-6">
          <div class="card p-3">
            <img class="cad-img-top" src="https://rickandmortyapi.com/api/character/avatar/1.jpeg" height="350px" alt="image character">
            <div class="card-body">
              <h5 class="card-tittle">Rick Grimes</h5>
            </div>
          </div>
        </div> 
        -->
      </div>
    </div>
  </main>
</template>

<style>
  
</style>