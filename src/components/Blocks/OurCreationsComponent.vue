<template>
    <section>
        <h3>Our creations</h3>
        <button>See all</button>
    </section>
</template>
<style scoped>
    section{
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    h3 {
        text-transform: uppercase;
        font-family: 'Josefin Sans', sans-serif;
        font-weight: 300;
        font-size: 50px;
    }

    button {
        width: 20%;
        padding: 10px;
        border: 2px solid;
        background-color: var(--white);
        text-transform: uppercase;
        font-family: 'Josefin Sans', sans-serif;
        font-weight: 600;
        font-size: 20px;
    }

    button:active {
        background-color: var(--black);
        color: var(--white);
    }

    button:hover {
        cursor: pointer;
    }

    @media (max-width:992px) {
        section{
            flex-direction: column;
        }

        h3{
            text-align: center;
        }

        button{
            width: 90%;
        }
    }
</style>