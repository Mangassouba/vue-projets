<template>

    <HelloWorldCompnents
    @update-name="name => display(name)"
    />

    <span>Bonjours, j'ai m'appelle {{ name }} et j'ai {{ age }} ans</span>
   
</template>



<script setup>
    import HelloWorldCompnents from './components/HelloWorldCompnents.vue';

    import { ref } from 'vue';

    const name = ref('NordCoders')
    const age = ref(29)


    const display = (name) => {
        console.log('App.vue : ' + name)
    }

</script>



<style scoped>
 .bold {
    font-weight: bolder;
 }

 .test-red{
    color: red;
 }

 .test-green{
    color: green;
 }
 span{
    display: block;
    color: green;
    margin-top: 10px;
 }

</style>
 