<template>
    <picture>
        <img :src="getImageUrl(imageUrl)" :alt="title">
    </picture>
    <p>{{title}}</p>
</template>
<script setup>
    const props = defineProps([
        'imageUrl',
        'title'
    ])

    const getImageUrl = (url) => new URL(url,import.meta.url).href
</script>
<style scoped>

    picture{
        position:relative;
    }

    p {
        position: relative;
        bottom: 20%;
        left: 20%;
        max-width: 200px;
        margin: 0;
        color: var(--white);
        text-transform: uppercase;
        font-family: 'Josefin Sans', sans-serif;
        font-weight: 600;
        font-size: 30px;
    }

    img{
        width: 100%;
        filter: brightness(60%);
        box-shadow: 1px 0 10px black;

    }

    img:hover{
        filter: brightness(80%);
    }

    @media (max-width:991px) {
        p{
            left: 5%;
            bottom: 30%;
            max-width: 500px;
            font-size: 50px;
            font-weight: 500;
        }
    }

    @media (max-width:600px) {
        p{
            left: 5%;
            bottom: 30%;
            max-width: 500px;
            font-size: 28px;
            font-weight: 500;
        }
    }
</style>