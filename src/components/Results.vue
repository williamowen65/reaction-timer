<template>
    <h4> Reaction time: {{ score }} ms </h4>
    <p class="rank"> {{ rank }} </p>
</template>

<script>
export default {
    props: ['score'],
    data() {
        return {
            rank: null
        }
    },
    mounted() {
        if(this.score < 250){ 
            this.rank = 'Ninja fingers';
        } else if (this.score < 400) {
            this.rank = 'Rapid reflexes';
        } else {
            this.rank = 'snail pace';
        }
    }
}
</script>

<style>
    .rank {
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }
</style>