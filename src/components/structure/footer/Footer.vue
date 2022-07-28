<template>
    <footer>

        <div class="link-section wrapper flex-between">

            <div class="footer-info footer-card">
                <Logo/>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
                <ul class="unstyled-list">
                    <li><i class="fa-solid fa-phone text-icon"></i>{{contacts.phone}}</li>
                    <li><i class="fa-solid fa-envelope text-icon"></i>{{contacts.mail}}</li>
                    <li><i class="fa-solid fa-location-dot text-icon"></i> {{contacts.address}}</li>
                </ul>
                <a href="#" class="btn btn-style2">GET IN TOUCH</a>

            </div>
            
            <div class="footer-links footer-card">
                <ListComponent
                :listTitle="'About'"
                :listLinks="aboutLinks"/>
            </div>

            <div class="footer-links footer-card">
                <ListComponent
                :listTitle="'Services'"
                :listLinks="servicesLinks"/>
            </div>

            <div class="footer-links footer-card">
                <ListComponent
                :listTitle="'Support'"
                :listLinks="supportLinks"/>
            </div>

        </div>

        <div class="copyrights-section">

            <div class="wrapper flex-between">
                <p>
                    Enjoy the low price. We are tracking any intention of piracy.
                </p>
                <p>
                    © 2020 NEXGEN is Proudly Powered by <a href="#">Codings</a>
                </p>
            </div>

        </div>

        <div>
            <button @click="scrollToTop" class="go-top-icon centered-circle-icon big-icon">
                <i class="fa-solid fa-arrow-up"></i>
            </button>
            <!-- Go to top arrow (position absolute bottom=0, right=0) -->
        </div>

    </footer>
</template>

<script>
import Logo from "../../elements/Logo.vue";
import ListComponent from "../../elements/ListComponent.vue";

export default {
    name : 'Footer',
    components : {
        Logo,
        ListComponent,
    },

    props : {
        contacts : Object,
    },

    data : function (){
        return {
            aboutLinks : [
                {
                    title : "The company",
                    url : "#"
                },
                {
                    title : "Institutional",
                    url : "#"
                },
                {
                    title : "Social & Events",
                    url : "#"
                },
                {
                    title : "Innovation",
                    url : "#"
                },
                {
                    title : "Environment",
                    url : "#"
                },
                {
                    title : "Technology",
                    url : "#"
                },
            ],

            servicesLinks : [
                {
                    title : "Audit & Assurance",
                    url : "#"
                },
                {
                    title : "Financial Advisory",
                    url : "#"
                },
                {
                    title : "Analytics M&A",
                    url : "#"
                },
                {
                    title : "Middle Marketing",
                    url : "#"
                },
                {
                    title : "Legal Consulting",
                    url : "#"
                },
                {
                    title : "Regulatory Risk",
                    url : "#"
                },
            ],

            supportLinks : [
                {
                    title : "Responsability",
                    url : "#"
                },
                {
                    title : "Terms of Use",
                    url : "#"
                },
                {
                    title : "About Cookies",
                    url : "#"
                },
                {
                    title : "Privacy Policy",
                    url : "#"
                },
                {
                    title : "Accessibility",
                    url : "#"
                },
                {
                    title : "Information",
                    url : "#"
                },
            ],
        }
    },

    methods : {
        
        scrollToTop : function(){
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }
    },
}
</script>

<style lang="scss">
@import '../../../assets/styles/generals.scss';
@import '../../../assets/styles/variables.scss';

    footer {
        /* TODO: Change to correct colors */
        background-color: $bgc3;
        color: $txtc2;
        position: relative;
    }

    .link-section {
        padding: 6rem 0;
    }

    .footer-card {
        width: calc((100% - 1rem * 2 * 4) / 4);
        margin: 0rem 1rem;
    }

    .footer-info {

        p, a {

            margin: 1.2rem 0rem;
        }

        ul {
            line-height: 1.6rem;
        }
    }

    .copyrights-section {
        font-size: 0.9rem;
        padding: 1rem;

        a {
            color: $brandColor;
        }
    }

    .go-top-icon {
        position: absolute;
        bottom: 5px;
        right: 5px;
        opacity: 0.1;

        &:hover {
            cursor: pointer;
            opacity: 0.7;
        }
    }

</style>