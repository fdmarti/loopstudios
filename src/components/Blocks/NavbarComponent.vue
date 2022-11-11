<template>
    <header>
        <nav>
            <picture class="logo">
                <img src="../../assets/images/logo.svg" alt="logo loop studios">
            </picture>
            <div class="hamburguer" @click="showSideBarMenu">
                <img class="hamburguer-icon" v-if="!sideBarMenu" src="../../assets/images/icon-hamburger.svg" alt="hamburguer icon">
                <img class="hamburguer-icon" v-else src="../../assets/images/icon-close.svg" alt="close menu icon">
            </div>
            <ul class="menu">
                <li class="menu-items">
                    <a href="#">About</a>
                    <a href="#">Careers</a>
                    <a href="#">Events</a>
                    <a href="#">Products</a>
                    <a href="#">Support</a>
                </li>
            </ul>
        </nav>
        <BannerComponent/>
    </header>
</template>
<script setup>
    import { ref } from '@vue/reactivity'
    import BannerComponent from '../Blocks/BannerComponent.vue'

    const sideBarMenu = ref(false);

    const showSideBarMenu = () => {
        sideBarMenu.value = !sideBarMenu.value

        const sideBarMenuOptions = document.querySelector('.menu');

        if ( sideBarMenu.value ){
            sideBarMenuOptions.style.display = 'block'
        }else{
            sideBarMenuOptions.style.display = 'none'
        }

    }
        
</script>
<style scoped>

header {
    background-image: url('../../assets/images/desktop/image-hero.jpg');
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center center;

    padding: 0 2rem 7rem 2rem;
}

nav {
    display: flex;
    align-items: center;
    justify-content: space-between;
    max-width: 1300px;
    margin: 0 auto;
    padding: 5rem 0;
}

.logo{
    z-index: 999;
}

.hamburguer{
    display: none;
    z-index: 999;
}

.hamburguer-icon{
    width: 150%;
}


@media (max-width:991px) {
    .hamburguer{
        display: block;
        position: absolute;
        top: 10%;
        right: 8%;
    }

    .menu{
        z-index: 998;
        display: none;
        overflow: hidden;
        position: absolute;
        height: 100vh;
        width: 100%;
        top: -5;
        right: 0;
        left: 0;
        bottom: -15px;
        padding: 250px 50px;
        background-color: #000;
    }

    .menu-items{
        flex-direction: column;
        position: absolute;
    }

    a{
        text-transform: uppercase;
        font-family: 'Josefin Sans', sans-serif;
    }
}

</style>