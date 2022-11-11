<template>
    <section>
        <picture>
            <img src="../../assets/images/desktop/image-interactive.jpg" alt="leader in interactive vr">
        </picture>
        <div class="content-leader">
            <h2>The leader in interactive vr</h2>
            <p>Founded in 2011, Loopstudios has been producing world-class virtual reality projects for some of the best companies around the globe. Our award-winning creations have trasnformed businesses through digital experiences that bind to ther brand.</p>
        </div>
    </section>
</template>
<style scoped>
    section{
        padding: 10rem 0;
        display: flex;
        position: relative;
    }

    .content-leader {
        position: relative;
        top: 200px;
        left: -150px;
        padding: 4rem 0 4rem 5rem;
        background-color: var(--white);
    }

    h2 {
        text-transform: uppercase;
        letter-spacing: 2px;
        font-family: 'Josefin Sans', sans-serif;
        font-weight: 300;
        font-size: 46px;
    }

    p {
        color: var(--darkGrey);
        font-family: 'Alata', sans-serif;
        line-height: 1.5;
    }

    @media (max-width:992px) {
        section{
            flex-direction: column;
            text-align: center;
            padding: 10rem 0 5rem 0;
        }

        img{
            width: 100%;
            padding: 0 20px;
        }

        .content-leader{
            top: 0;
            left: 0;
            padding: 20px;
            margin: 0 auto;
            max-width: 700px;
        }

        h2{
            font-size: 55px;
        }

        p{
            line-height: 1.8;
        }
    }

    @media (max-width:600px) {
        section{
            padding: 5rem 0;
        }
        h2{
            font-size: 35px;
        }
    }
</style>