/* eslint-disable */
<template>
 <div>
    <h2>Place :- {{tourist_place.place}}</h2>
    <h2>Rating :- {{tourist_place.rating}}</h2>
    <h2>Price :- {{tourist_place.price}}</h2>
    <h2>About :- {{tourist_place.about}}</h2>
    <h4>City :-{{tourist_place.city}}</h4>

    </div>
</template>

<script>

export default{
    name: 'Tourist_place',
    props:{
        tourist_place: Array
    }
}
</script>

<style scoped>



h4{
    margin: 1px;
}

div{
    background-color : #d7a452;
    color : black;
    padding : 1em;
    text-align: center;
}




</style>
