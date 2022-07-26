<template>
    <header>
        <SocialBar
        :contacts = "contacts"/>
        <div class="main-header">
            <div class="header-items">
                <Navbar class="wrapper"/>
                <div class="hero-text wrapper">
                    HERO TEXT
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
@import '../assets/styles/generals.scss';
@import '../assets/styles/variables.scss';

    .main-header {
        background-image: url("../assets/img/hero-image.png");
        background-size: cover;
    }

    .header-items {
        background-color: rgba(0,0,0,0.6);
    }




</style>