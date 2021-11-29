<template>
    <div class="container mt-5">
        <liste v-bind:myArr="myArr"></liste>   
    </div>
</template>

<script>
import Liste from './Liste.vue'

export default {
    name: 'Contenu',
    data: function(){
        return {
            myArr: [
                {titre: 'Inception',date: 2010},
                {titre: 'Avatar',date: 2009},
                {titre: 'Seven',date: 1995},               
            ]
        }
    },
    components: {
        'liste': Liste
    }
}
</script>

<style scoped>

</style>

