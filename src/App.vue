<template>
  <ParentToChildData/>
  <hr>
  <FormInputs/>
  <hr>
  <HelloWorld msg="Welcome to Your first Vue.js App" />
  <hr>
  <Home/>

</template>

<script>
import FormInputs from './components/FormInputs.vue';
import HelloWorld from './components/HelloWorld.vue'
import Home from './components/Home.vue';
import ParentToChildData from './components/ParentToChildData.vue';

export default {
    name: 'App',
    components: {
    HelloWorld,
    // Hello,
    Home,
    FormInputs,
    ParentToChildData
}
}
</script>


