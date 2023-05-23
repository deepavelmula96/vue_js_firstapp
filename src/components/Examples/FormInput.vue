<template lang="">
    <div>
        <input type="text" v-model="userName"/>
        <br>
        {{userName}}
    </div>
</template>
<script>
export default {
    name:"FormInput",
    data(){
        return{
userName:null
        }
    }

}
</script>
<style lang="">
    
</style>