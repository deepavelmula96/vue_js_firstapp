<template>
<h3>Parent to Child Data</h3>
<Child :name="name" :data="user" :getDetail="getDetails" />
</template>

<script>
import Child from './Child.vue';

export default {
    name: "ParentToChildData",
    components: {
        Child
    },
    data(){
        return{
            name:'deepa',
            user:{
                name:"deepa _rao",
                email:"deepa@gmail.com"
            }
        }
    },
    methods:{
        getDetails(){
            alert("function called")
        }
    }
}
</script>
