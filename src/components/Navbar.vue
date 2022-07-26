<template>
    <nav class="flex-between">
        <Logo/>
        <ul class="flex-between unstyled-list">
            <li v-for="(item, index) in navItems" :key="index">
                <a :href="item.url">{{item.name}}</a>
            </li>
            <li>
                <button>PRESS ME</button>
            </li>
        </ul>
    </nav>
</template>

<script>
import Logo from './Logo.vue';

export default {

    name : "Navbar",
    components : {
        Logo,
    },

    data : function(){
        return{
            navItems : [
                {
                    name : "home",
                    url : "#"
                },
                {
                    name : "about",
                    url : "#"
                },
                {
                    name : "services",
                    url : "#"
                },
                {
                    name : "pricing",
                    url : "#"
                },
                {
                    name : "blog",
                    url : "#"
                },

            ]
        }
    }

}
</script>

<style lang="scss">
@import '../assets/styles/generals.scss';
@import '../assets/styles/variables.scss';

    nav {
        padding: 1rem 0rem;

        ul {
            text-transform: uppercase;
        }
        
        li {
            margin: 1rem;

            a {
                color: #FFF;
            }
        }
    }

</style>