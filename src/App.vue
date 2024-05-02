<script setup>
  import {ref} from 'vue'
  let num = ref(0)

</script>

<template>
  <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
    <div class="container-fluid">
      <router-link class="navbar-brand" to="/">
        <img src="../public\Rick_and_Morty.svg.png" alt="Logo" width="250" height="auto" class="d-inline-block align-text-top">
      </router-link>
      <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item">
            <router-link class="nav-link" aria-current="page" to="/"><i class="bi bi-houses-fill"></i> HOME</router-link>
          </li>
          <li class="nav-item">
            <router-link class="nav-link" to="/about"><i class="bi btn-lg bi-file-earmark-person-fill"></i> ABOUT</router-link>
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
@import url("https://cdn.jsdelivr.net/npm/bootstrap-icons@1.11.3/font/bootstrap-icons.min.css");

.navbar{
  font-size: 25px;
}

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
  background-color: #4B4453;
}

@media screen and (max-width: 576px) {
  .card{
    flex-direction: column;
  }
}

.card ul li{
  font-size: 18px;
}

.data-about{
  display: flex;

}

.data{
  font-size: 25px;
  padding-bottom: 20px;
}

</style>