<template>
<div>
    <ul class="liste">
        <li v-for="(film, index) in myArr" v-bind:key="index">
           <div class="card">
               <div class="card-body">
                    Titre : {{ film.titre }}
                    <br>
                    Date : {{ film.date }}
               </div>
           </div>
        </li>
    </ul>
    <div v-on:click="supprFilm" class="btn btn-danger mt-2">Supprime le film</div>
</div>

</template>


<script>

export default {
    name: 'Liste',
    data(){
        return{
            fruits: ['Orange','Papaye','Fraise']
        }
    },
    methods: {
        supprFilm: function(){
            this.myArr.pop()
        }
    },
    props: ['myArr']
}

</script>

<style scoped src="./Liste/Liste.css"></style>
