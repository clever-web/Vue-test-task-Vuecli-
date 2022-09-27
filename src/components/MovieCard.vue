<template>
    <div class="card" v-on:click="goToDetailsPage(movie.id)">
        <div class="card-hover card-body">
            <div :style="{'background-image': `url(${movie.poster})`}"  class="card-cover-img"></div>
            <p class="card-title">{{movie.name}}</p>
            <p class="card-description">{{movie.description}}</p>
            <div class="badges">
                <ul class="badges-list d-flex">
                    <li :class="`badge-item ${(movie.rating < 4 && movie.rating > 0 && 'badge-red')
                        || (movie.rating < 7 && movie.rating > 4 && 'badge-purple') 
                        || (movie.rating < 10 && movie.rating > 7 && 'badge-success')}`">
                        <img src="../assets/icons/score.png" class="badge-icon" />
                        <a href="" class="badge-text rating">{{movie.rating}}</a></li>
                    <li class="badge-item badge-blue"><img src="../assets/icons/genre.png" class="badge-icon" />
                        <a href="" class="badge-text genre">{{movie.genre}}</a></li>
                    <li class="badge-item badge-purple"><img src="../assets/icons/duration.png" class="badge-icon" />
                        <a href="" class="badge-text duration">{{movie.duration}}</a></li>
                </ul>
            </div>
        </div>
    </div>
    
</template>

<script>
    export default {
        name: "movie-card",
        props: {
            movie: Object,
        },
        methods: {
            goToDetailsPage: function(id) {
                this.$router.push("/" + id);
            },
        }
    }
</script>

<style scoped>
    @import "../assets/styles/common.css";
</style>