<script setup>
const pokemon = defineProps(["name","xp","height","img","loading","weight"])


</script>

<template>
    <div class="card cardlistpokemon" :class=" loading ? '' :'animate__animated animate__flip'">
      
            <img
            v-if="pokemon.name"
            :src="pokemon.img"  
            height="250" 
            class="card-img-top pt-2" 
            :alt="pokemon.name ">

            <img
            v-else
            src="../assets/egg_pokemon.svg"  
            height="250" 
            class="card-img-top pt-2" 
            :alt="'???'"
            >



            <div class="card-body">
              <h5 class="card-title text-center">{{ pokemon.name || '???'}}</h5>
              <hr>
              <div class="row">
                <section class="col">
                    <strong>XP: </strong>
                    <span>{{ pokemon.xp }}</span>
                </section>
                <section class="col">
                    <strong>Altura:</strong>
                    <span>{{ pokemon.height }}</span>
                </section>
                <section class="col">
                    <strong>Peso:</strong>
                    <span>{{ pokemon.weight }}</span>
                </section>
              </div>
            </div>
          </div>

</template>

<style scoped>
 .cardlistpokemon{
    height: 550px;
    background: rgb(2,0,36);
    background: linear-gradient(90deg, rgba(2,0,36,1) 0%, rgba(121,9,98,0.9136029411764706) 12%, rgba(0,212,255,1) 100%);
    color: aliceblue;
 }
</style>