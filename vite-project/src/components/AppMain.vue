<script>
import axios from 'axios';
    export default {
        data() {
            return {
            }
        }
    },
    methods:{
        getSearch(){
            axios.get('https://api.themoviedb.org/3/search/movie&api_key=17cd8953610657dd6b2e079f297555fe')
            .then((response) => {
            console.log();
            })
            .catch(function(error) {
            console.log(error);
            });
        },

    }
</script>

<template>

</template>

<style scoped>

</style>
