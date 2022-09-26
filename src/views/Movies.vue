<template>
    <div class="home">
        <div class="container-fluid">
            <div class="row">
                <div 
                    class="col"
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
                console.log("ddddddddddddddd")
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