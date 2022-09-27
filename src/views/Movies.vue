<template>
    <div class="home">
        <Header />
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
        <Footer />
    </div>
</template>

<script>
// @ is an alias to /src
import Header from "@/layouts/Header.vue";
import Footer from "@/layouts/Footer.vue";
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
            movielist: []
        };
    },
    components: {
    MovieCard,
    Header,
    Footer
},
}
</script>
<style>
    @import "../assets/styles/common.css";
</style>