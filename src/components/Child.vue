<template>
    <h3>child Component</h3>
    <h2>{{ name }}</h2>
    <h2>{{data.name +"      email is " +data.email}}</h2>
    <button v-on:click="getDetail()">Click</button>
</template>
<script>
export default{
    name:"Child",
    props:{
        name:String,
        data:Object,
        getDetail:Function
    }
}
</script>