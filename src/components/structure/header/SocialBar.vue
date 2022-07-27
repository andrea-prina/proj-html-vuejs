<template>
    <div id="social-bar">
        <div class="wrapper flex-between">
            <div><i class="fa-solid fa-clock text-icon"></i>Open Hours: {{openHours}}</div>
            <div id="contacts">
                <div><i class="fa-solid fa-envelope text-icon"></i>{{contacts.mail}}</div>
                <div><i class="fa-solid fa-phone text-icon"></i>{{contacts.phone}}</div>
                <div v-for="(social, index) in socials" :key="index">
                    <a :href="social.url"><i :class="social.icon"></i></a>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name : 'SocialBar',

    props : {
        contacts : Object,
    },

    data : function(){
        return {
            openHours : "Mon - Sat - 9:00 - 18:00",

            socials : [
                {
                    icon: "fa-brands fa-facebook-f",
                    url: "#"
                },
                {
                    icon: "fa-brands fa-twitter",
                    url: "#"
                },
                {
                    icon: "fa-brands fa-linkedin-in",
                    url: "#"
                },
            ]
        }
    }

}
</script>

<style lang="scss">

@import '../../../assets/styles/generals.scss';
@import '../../../assets/styles/variables.scss';

    #social-bar {
        background-color: $bgc4;
        padding: 1rem 0;
        font-size: 0.9rem;

        &, a {
            color: $darkbgSecondaryText;
        }
    }

    #contacts {
        display: flex;
        justify-content: space-around;
        gap: 1.5rem;
    }



</style>