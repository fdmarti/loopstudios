<template>
    <section>
        <div v-for="(card,index) in cardsColection" :key="index">
            <CardImageComponent :imageUrl=" sizeScreen > 991 ? card.urlDesktop : card.urlMobile" :title="card.title"/>
        </div>
    </section>
</template>
<script setup>
    import CardImageComponent from '../CardImageComponent.vue'
    import { ref } from '@vue/reactivity'
    import { onMounted } from '@vue/runtime-core'

    const sizeScreen = ref(document.documentElement.clientWidth)

    const getDimentions = () => {
        sizeScreen.value = document.documentElement.clientWidth
    }

    onMounted(() => {
        window.onresize = () => getDimentions()
    })

    const cardsColection = [
        {
            title: 'Deep Earth', 
            urlDesktop: '../assets/images/desktop/image-deep-earth.jpg', 
            urlMobile: '../assets/images/mobile/image-deep-earth.jpg'
        },
        {
            title: 'Night Arcade', 
            urlDesktop: '../assets/images/desktop/image-night-arcade.jpg', 
            urlMobile: '../assets/images/mobile/image-night-arcade.jpg'
        },
        {
            title: 'Soccer Team vr', 
            urlDesktop: '../assets/images/desktop/image-soccer-team.jpg', 
            urlMobile: '../assets/images/mobile/image-soccer-team.jpg'
        },
        {
            title: 'The grid', 
            urlDesktop: '../assets/images/desktop/image-grid.jpg', 
            urlMobile: '../assets/images/mobile/image-grid.jpg'
        },
        {
            title: 'From up above vr', 
            urlDesktop: '../assets/images/desktop/image-from-above.jpg', 
            urlMobile: '../assets/images/mobile/image-from-above.jpg'
        },
        {
            title: 'Pocket Borealis', 
            urlDesktop: '../assets/images/desktop/image-pocket-borealis.jpg', 
            urlMobile: '../assets/images/mobile/image-pocket-borealis.jpg'
        },
        {
            title: 'The curiosity', 
            urlDesktop: '../assets/images/desktop/image-curiosity.jpg', 
            urlMobile: '../assets/images/mobile/image-curiosity.jpg'
        },
        {
            title: 'Make it Fisheye', 
            urlDesktop: '../assets/images/desktop/image-fisheye.jpg', 
            urlMobile: '../assets/images/mobile/image-fisheye.jpg'
        },
    ]

</script>
<style scoped>
    section {
        display: grid;
        padding: 2rem 0;

        gap: 2rem;
        grid-template-columns: repeat(4,1fr);
    }

    @media (max-width:991px) {
        section{
            margin-top: 35px;
            grid-template-columns: 1fr;
            padding: 1rem 2rem;
            gap: 0;
        }
    }

</style>
