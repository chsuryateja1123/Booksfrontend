/* eslint-disable */
<template>

     <div class="bookbox">

        <div v-for="tourist_place in tourist_places" :key="tourist_place.id" >

                <Tourist_place :tourist_place="tourist_place"/>
        </div>


     </div>

</template>

<script>

import Tourist_place from "./Book.vue"
export default{

    name: 'Bookbox',
    components: {
        Tourist_place
    },
    props: {
      tourist_places: Array
    }

}

</script>


<style>

.bookbox{
    background-color: #F9EBC8;
    padding: 1em;
    color: black;
}
</style>