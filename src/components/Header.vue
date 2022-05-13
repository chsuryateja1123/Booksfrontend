/* eslint-disable */
<template>
<div>
    <h1> {{heading}} </h1>

</div>
</template>

<script>

export default{
    name: 'Header',
    props:{
       heading: String,

    }
}

</script>

<style scoped>

div{
    text-align: center;
}

</style>