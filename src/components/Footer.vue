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
            <!-- Copyright -->
        </div>

        <div>
            <!-- Go to top arrow (position absolute bottom=0, right=0) -->
        </div>

    </footer>
</template>

<script>
import Logo from "./Logo.vue";
import ListComponent from "./ListComponent.vue";

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
                    title : "",
                    url : ""
                },
            ],

            supportLinks : [
                {
                    title : "",
                    url : ""
                }
            ]
        }
    }
}
</script>

<style lang="scss">

    footer {
        /* TODO: Change to correct colors */
        background-color: black;
        color: white;
    }

    .link-section {
        padding: 3rem 0;
    }

    .footer-card {
        width: calc((100% - 2rem * 2 * 4) / 4);
        border: 1px solid red;
        margin: 0rem 2rem;
    }

</style>