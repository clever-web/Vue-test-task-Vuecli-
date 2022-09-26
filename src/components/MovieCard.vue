<template>
    <div>
        <div class="card-body">
            <div :style="{'background-image': `url(${movie.poster})`}"  class="card-cover-img"></div>
            <p class="card-title">{{movie.name}}</p>
            <p class="card-description">{{movie.description}}</p>
            <div class="tags">
                <ul class="badges-list">
                    <li><a href="">{{movie.rating}}</a></li>
                    <li><a href="">{{movie.genre}}</a></li>
                    <li><a href="">{{movie.duration}}</a></li>
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
    }
</script>

<style scoped>
    @import "../assets/styles/common.css";
</style>