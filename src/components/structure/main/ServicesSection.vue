<template>
    <section id="services-section">
        <div class="wrapper">
            <SectionTitle :titleData="sectionTitleInfo"/>
            <div class="flex-between flex-wrap cards">
                <FeatureCard v-for="(card, index) in serviceCards" :key="index" :cardInfo="card"/>
            </div>
        </div>
    </section>
</template>

<script>
import SectionTitle from '../../elements/SectionTitle.vue'
import FeatureCard from '../../elements/FeatureCard.vue'

export default {

    name : "ServicesSection",

    components : {
        SectionTitle,
        FeatureCard,
    },

    data : function(){
        return{
            sectionTitleInfo : {
                
                smallTitle : "Our business areas",
                preHighlightTitle : "Excellence in",
                highlightTitle : "Services",
                postHighlightTitle : "",
                paragraph : "lorem ipsum dolor sit amet lorem ipsum dolor sit amet",
                style : "dark",
                button : {
                    text : "SEE ALL",
                    url : "#"
                }
            },

            serviceCards : [
                {
                    icon : "fa-solid fa-sitemap",
                    title : "Audit & Assurance",
                    paragraph : "Lorem ipsum dolor, sit amet consectetur adipisicing elit.",
                    style : "dark",
                    button : {
                        text : "READ MORE",
                        url : "#"
                    }
                },
                {
                    icon : "fa-solid fa-briefcase",
                    title : "Financial Advisory",
                    paragraph : "Lorem ipsum dolor, sit amet consectetur adipisicing elit.",
                    style : "dark",
                    button : {
                        text : "READ MORE",
                        url : "#"
                    }
                },
                {
                    icon : "fa-solid fa-chart-simple",
                    title : "Analytics and M&A",
                    paragraph : "Lorem ipsum dolor, sit amet consectetur adipisicing elit.",
                    style : "dark",
                    button : {
                        text : "READ MORE",
                        url : "#"
                    }
                },
                {
                    icon : "fa-solid fa-plane-up",
                    title : "Middle Marketing",
                    paragraph : "Lorem ipsum dolor, sit amet consectetur adipisicing elit.",
                    style : "dark",
                    button : {
                        text : "READ MORE",
                        url : "#"
                    }
                },
                {
                    icon : "fa-solid fa-globe",
                    title : "Legal Consulting",
                    paragraph : "Lorem ipsum dolor, sit amet consectetur adipisicing elit.",
                    style : "dark",
                    button : {
                        text : "READ MORE",
                        url : "#"
                    }
                },
                {
                    icon : "fa-solid fa-book",
                    title : "Regulatory Risk",
                    paragraph : "Lorem ipsum dolor, sit amet consectetur adipisicing elit.",
                    style : "dark",
                    button : {
                        text : "READ MORE",
                        url : "#"
                    }
                },
            ]
        }
    }

}
</script>

<style lang="scss" scoped>
@import '../../../assets/styles/generals.scss';
@import '../../../assets/styles/variables.scss';

    #services-section {
        background-color: $bgc3;
    }

    .cards {
        margin-top: 1rem;
    }

</style>