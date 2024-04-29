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
      </div>
    </div>
  </main>
</template>

<style>
  
</style>