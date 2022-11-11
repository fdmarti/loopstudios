<template>
    <footer>
        <section>
            <div class="menu">
                <picture>
                    <img src="../../assets/images/logo.svg" alt="logo loopestudio">
                </picture>
                <ul>
                    <li class="links">
                        <a href="#">About</a>
                        <a href="#">Careers</a>
                        <a href="#">Events</a>
                        <a href="#">Products</a>
                        <a href="#">Support</a>
                    </li>
                </ul>
            </div>
            <div>
                <ul>
                    <li class="icons">
                        <i class='bx bxl-facebook-square bx-md'></i>
                        <i class='bx bxl-twitter bx-md'></i>
                        <i class='bx bxl-pinterest bx-md' ></i>
                        <i class='bx bxl-instagram bx-md' ></i>
                    </li>
                </ul>
                <p>© 2022 Loopstudios. All rights reserved.</p>
            </div>
        </section>
    </footer>
</template>
<style scoped>
section {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

footer {
    padding: 50px;
    background: var(--black);
    color: var(--white);
}

ul {
    margin: 30px 0 0 0;
    padding: 0;
}

p {
    color: var(--darkGrey);
    font-family: 'Alata', sans-serif;
}

.icons{
    justify-content: end;
    gap: 1rem;
}

i:hover{
    cursor: pointer;
}

.bxl-facebook-square:hover{
    color: #4267B2;
}

.bxl-twitter:hover{
    color: #1DA1F2;
}

.bxl-pinterest:hover{
    color: #E60023;
}

.bxl-instagram:hover{
    color: var(--white);
    background: linear-gradient(90deg, rgba(64,93,230,1) 0%, rgba(91,81,216,1) 17%, rgba(131,58,180,1) 34%, rgba(193,53,132,1) 53%, rgba(225,48,108,1) 70%, rgba(253,29,29,1) 86%, rgba(245,96,64,1) 100%);
    border-radius: 30%;
}

@media (max-width:991px) {
    section{
        flex-direction: column;
    }

    .menu{
        display: flex;
        flex-direction: column;
    }

    .links{
        display: flex;
        flex-direction: column;
        text-align: center;
    }

    .icons{
        justify-content: center;
    }

}

@media (max-width:600px) {
    p{
        text-align: center;
    }
}
</style>