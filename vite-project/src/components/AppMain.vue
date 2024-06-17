<script>
import axios from 'axios';
    export default {
        data() {
            return {
            }
        },
        methods:{
        getSearch(){
            axios.get('https://api.themoviedb.org/3/search/movie&api_key=17cd8953610657dd6b2e079f297555fe')
            .then((response) => {
                this.search = response.data.results;
                console.log(this.search);
            })
            .catch(function(error) {
            console.log(error);
            });
        },
        created(){
        this.getSearch()

        },
    }
}

</script>

<template>
    <main>
       
        <ul v-for="search in search" :key="search.id">
            <li>{{ search.title }}</li>
            <li>{{ search.original_language }}</li>
            <li>{{ search.original_title }}</li>
            <li>{{ search.vote_average }}</li>
        </ul>
    </main>

</template>

<style scoped>

</style>
