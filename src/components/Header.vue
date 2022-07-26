<template>
    <header>
        <SocialBar
        :contacts = "contacts"/>
        <div class="main-header">
            <img class="header-img" src="../assets/img/hero-image.png" alt="">

            <div class="header-items wrapper">
                <nav>
                    NAVBAR
                    <!-- Navbar -->
                </nav>
                <div class="hero-text">
                    HERO TEXT
                </div>
            </div>

        </div>
    </header>
</template>

<script>
import SocialBar from './SocialBar.vue'

export default {
    name : 'Header',

    props : {
        contacts: Object,
    },

    components : {
        SocialBar,
    }

}
</script>

<style lang="scss">
@import '../assets/styles/generals.scss';
@import '../assets/styles/variables.scss';

    .main-header {
        height: 400px;
        position: relative;
    }

    .header-img {
        filter: brightness(0.5) saturate(75%);
        object-fit: cover;
        width: 100%;
    }

    .header-items {
        position: absolute;
        top: 0;
        left: 0;
        right: 0;
    }

    .hero-text {
        text-align: center;
        padding: 8rem;
        border: 1px solid red;
    }



</style>