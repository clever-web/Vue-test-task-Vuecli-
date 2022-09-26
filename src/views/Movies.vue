<template>
    <div class="home">
        <div class="container-fluid">
            <div class="row">
                <div 
                    class="col-sm-12 col-md-4 col-lg-3 mb-4"
                    v-for="movie in movielist"
                    :key="movie.id"
                >
                    <MovieCard :movie="movie" />
                </div>
            </div>
        </div>
    </div>
</template>

<script>
// @ is an alias to /src
import MovieCard from "@/components/MovieCard.vue";
import axios from "axios";

export default {
    name: "vue-movies",
    mounted() {
        axios({
            method: "GET",
            url: "assets/json/movielist.json",
        }).then(
            (response) => {
                this.movielist = response.data;
            },
            (error) => {
                console.error(error)
            }
        );
    },
    data() {
        return {
            movielist: [],
            selectedMovie: "",
        };
    },
    components: {
        MovieCard,
    },
}
</script>
<style>
    @import "../assets/styles/common.css";
</style>