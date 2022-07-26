<template>
    <header>
        <SocialBar
        :contacts = "contacts"/>
        <div>
            <nav>
                <!-- Navbar -->
            </nav>
            <div>
                <!-- Hero text -->
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


</style>