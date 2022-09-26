<template>
    <div>
        <div class="card-body">
            <div class="card-cover-img"></div>
            <div class="card-title"></div>
            <div class="card-description"></div>
            <div class="tags">
                <ul>
                    <li><a href="">Score</a></li>
                    <li><a href="">Genre</a></li>
                    <li><a href="">Duration</a></li>
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