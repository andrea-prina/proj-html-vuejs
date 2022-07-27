<template>
    <header>
        <SocialBar
        :contacts = "contacts"/>
        <div class="main-header">
            <div class="header-items">
                <Navbar class="wrapper"/>
                <div class="hero-text wrapper">
                    <h1>Lead ~ Customer</h1>
                    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Impedit minima doloribus nulla enim architecto? Praesentium qui quaerat rem laborum mollitia beatae, fuga, sequi a nesciunt officiis minus commodi. Maiores, deserunt.</p>
                    <a href="#" class="btn btn-style1">GET IN TOUCH</a>
                    <a href="#" class="btn btn-style2">READ MORE</a>
                </div>
            </div>

        </div>
    </header>
</template>

<script>
import SocialBar from './SocialBar.vue';
import Navbar from './Navbar.vue';

export default {
    name : 'Header',

    props : {
        contacts: Object,
    },

    components : {
        SocialBar,
        Navbar,
    }

}
</script>

<style lang="scss">
@import '../../../assets/styles/generals.scss';
@import '../../../assets/styles/variables.scss';

    .main-header {
        background-image: url("../../../assets/img/hero-image.png");
        background-size: cover;
        background-position: center;
    }

    .header-items {
        background-color: rgba(0,0,0,0.75);
    }

    .hero-text {
        padding: 10rem;
        text-align: center;
        color: #FFF;

        h1 {
            font-size: 4rem;
            font-family: 'Alfa Slab One', cursive;
        }

        p {
            margin: 2rem 0rem;
        }

        .btn {
            margin: 0 .5rem;
        }
    }




</style>