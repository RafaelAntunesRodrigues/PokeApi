<script setup>
const pokemon = defineProps(["name",'urlBaseSvg'])
</script>

<template>
    <div class="col-4">
        <div class="card p-2 mb-3 cardlistPokemon">
            <p class="text-center"> {{ pokemon.name }}</p>
            <img :src="urlBaseSvg" class="card-img-top" alt="..." height="80">
            
        </div>
    </div>

</template>

<style scoped>
.cardlistPokemon{
    background: rgb(2,0,36);
    background: linear-gradient(90deg, rgba(2,0,36,1) 0%, rgba(121,9,98,0.9136029411764706) 12%, rgba(0,212,255,1) 100%);
    cursor: pointer;
}
.cardlistPokemon:hover{
    background: rgb(2,0,36);
    background: linear-gradient(90deg, rgba(2,0,36,1) 0%, rgba(121,9,98,) 12%, rgba(0,212,255,2) 100%);
    cursor: pointer;
}
.cardlistPokemon img:hover{
   padding: .2rem;
}

</style>