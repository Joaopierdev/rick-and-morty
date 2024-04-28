<script setup>
  import {ref} from 'vue'
  let num = ref(0)

</script>

<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
      <router-link class="navbar-brand" to="/">
        <img src="" alt="Logo" width="30" height="24" class="d-inline-block align-text-top">
        Rick and Morty API
      </router-link>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <router-link class="nav-link active" aria-current="page" to="/">Home</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/about">Sobre</router-link>
          </li>
        </ul>
      </div>
    </div>
  </nav>

<div class="main">
  <router-view></router-view>
</div>

<footer class="bg-dark text-light">
  Desenvolvido por João Gabriel | 
  ADS - Unimar | 
  {{new Date().getFullYear()}}
</footer>

</template>

<style>
  footer{
    position: fixed;
    bottom: 0;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 46px;
  }
  
  body{
    background-color: rgb(39, 43, 51);
  }

  .card{
    display: flex;
    flex-direction: row;
  }
</style>