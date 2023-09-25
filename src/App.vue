<script>
import {ref} from 'vue'

let num = ref(0)
</script>


<template>
   <nav class="navbar navbar-expand-lg navbar-dark bg-primary">
  <div class="container-fluid">
    <router-link class="navbar-brand" to="#">
      <img src="https://cdn-icons-png.flaticon.com/512/188/188987.png" alt="Logo" width="30" height="24" class="d-inline-block align-text-top">
      Pokedex
    </router-link>
    
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav" aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
      <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
      <ul class="navbar-nav">
        <li class="nav-item">
          <router-link class="nav-link" aria-current="page" to="/">Home</router-link>
        </li>
        <li class="nav-item">
          <router-link class="nav-link" to="/about">About</router-link>
        </li>

      </ul>
    </div>
  </div>
</nav>

<!--CONTENT-->
<div class="main">
  <router-view> </router-view>
</div>

<footer class="bg-primary text-light"> 
  <div>
    {{ new Date().getFullYear() }}
  </div>
</footer>
</template>

<style>

 body{
  background: rgb(216,237,237);
  background: linear-gradient(90deg, rgba(216,237,237,0.9136029411764706) 12%, rgba(195,221,232,1) 55%, rgba(164,189,240,1) 100%);
 }

footer{
  position: fixed;
  bottom: 0;
  width: 100%;
  display: flex;
  align-items: center;
  justify-content: center;
  height: 56px;
}
</style>